<script>
  import { Message, Dialog, Input, Form, FormItem } from '@ggchivalrous/db-ui';
  import './index.scss';
  import { createEventDispatcher } from 'svelte';

  export let visible = false;

  const dispatch = createEventDispatcher();
  const fontForm = {
    name: '',
    path: '',
    isAutoName: false,
  };

  function close() {
    visible = false;
  }

  async function onFormSubmit() {
    const name = fontForm.name.trim();
    if (!name || !fontForm.path) {
      Message.info('请填写完整');
      return;
    }

    const res = await window.api.addFont(fontForm);

    if (res.code === 0) {
      switch (res.data) {
        case 1:
          Message.error('名称重复');
          return;
        case 2:
          Message.error('字体文件不存在');
          return;
        default:
          Message.success('添加成功');
          break;
      }
    }
    dispatch('update');
    close();
  }

  function onFileChange(ev) {
    if (ev.target && ev.target.type === 'file') {
      const files = ev.target.files;
      fontForm.path = files[0].path;
      if (!fontForm.name || fontForm.isAutoName) {
        fontForm.isAutoName = true;
        const arr = files[0].name.split('.');

        if (arr.length > 1) {
          arr.pop();
        }

        fontForm.name = arr.join('.');
      }
    }
  }

  function onNameChange() {
    if (fontForm.name) {
      fontForm.isAutoName = false;
    }
  }
</script>

<Dialog bind:visible width="400px" class="font-dialog">
  <Form>
    <FormItem label="字体名称">
      <Input
        type="text"
        bind:value={fontForm.name}
        placeholder="Enter name..."
        on:change={onNameChange}
      />
    </FormItem>
    <FormItem label="字体文件">
      <input class="font-input-file grass" type="file" on:change={onFileChange} />
    </FormItem>
  </Form>

  <footer class="modal-footer">
    <button class="grass button" on:click={close}>取消</button>
    <button class="grass button" on:click={onFormSubmit}>添加</button>
  </footer>
</Dialog>
