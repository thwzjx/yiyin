<script lang="ts">
  import { Drawer } from '@ggchivalrous/db-ui';
  import type { ICameraInfo, IFieldInfoItem } from '@web/main/interface';
  import { config } from '@web/store/config';
  import { tick } from 'svelte';

  import CustomParamDialog from '../custom-param-dialog/index.svelte';

  import ActionItem from './action-item.svelte';

  export let visible = false;
  export let beforeClose: any = null;

  let option: ICameraInfo;
  let flag = Date.now();
  const form: IFieldInfoItem = {
    use: false,
    value: '',
    bImg: '',
    wImg: '',
    type: 'text',
    param: undefined,
  };
  const dialog: {
    form: IFieldInfoItem<string | number | boolean>
    title: string
    showImg: boolean
    showType: boolean
    show: boolean
    field: keyof ICameraInfo
  } = {
    title: '',
    showImg: false,
    showType: false,
    show: false,
    field: 'Model',
    form: {
      use: false,
      value: '',
      bImg: '',
      wImg: '',
      type: 'text',
      param: undefined,
    },
  };
  const fieldMap: Record<keyof ICameraInfo, {
    showImg?: boolean
    showType?: boolean,
  }> = {
    Force: {
      showImg: false,
      showType: false,
    },
    Make: {
      showImg: true,
      showType: true,
    },
    Model: {
      showImg: true,
      showType: true,
    },
    ExposureTime: {
      showImg: false,
      showType: false,
    },
    FNumber: {
      showImg: false,
      showType: false,
    },
    ISO: {
      showImg: false,
      showType: false,
    },
    FocalLength: {
      showImg: false,
      showType: false,
    },
    ExposureProgram: {
      showImg: false,
      showType: false,
    },
    DateTimeOriginal: {
      showImg: false,
      showType: false,
    },
    LensModel: {
      showImg: true,
      showType: true,
    },
    LensMake: {
      showImg: true,
      showType: true,
    },
    PersonalSign: {
      showImg: true,
      showType: true,
    },
  };

  $: onTemplateFieldInfoChange($config.templateFieldInfo);

  async function onTemplateFieldInfoChange(templateFieldInfo: typeof $config.templateFieldInfo) {
    await tick();
    option = JSON.parse(JSON.stringify(templateFieldInfo));
  }

  function onUseChange(field: keyof ICameraInfo) {
    return async (e: CustomEvent<any>) => {
      const data: IFieldInfoItem = e.detail;
      config.update((v) => {
        v.templateFieldInfo[field].use = data.use;
        return v;
      });
    };
  }

  function onEdit(field: keyof ICameraInfo) {
    return async (e: CustomEvent<IFieldInfoItem & { title: string }>) => {
      dialog.field = field;
      dialog.form = { ...form, ...e.detail };
      if (fieldMap[field]) {
        dialog.showImg = fieldMap[field].showImg;
        dialog.showType = fieldMap[field].showType;
      }
      dialog.title = e.detail.title;
      dialog.show = true;
    };
  }
</script>

<Drawer
  size="500px"
  title="参数设置"
  bind:visible
  direction="rtl"
  {beforeClose}
  modal={false}
>
  <ActionItem title="强制使用" showSwitch showEdit={false} data={option.Force} on:use-change={onUseChange('Force')}>
    <svelte:fragment slot="popup">
      是否强制使用自定义参数作为最终输出
      <br>
      <b>开启:</b> 将强制使用自定义参数覆盖原始参数
      <br>
      <b>关闭:</b> 当对应的参数无法识别将使用自定义参数
    </svelte:fragment>
  </ActionItem>
  <ActionItem imgFlag={flag} title="个性签名" showSwitch data={option.PersonalSign} on:use-change={onUseChange('PersonalSign')} on:edit={onEdit('PersonalSign')} />
  <ActionItem imgFlag={flag} title="厂商" showSwitch data={option.Make} on:use-change={onUseChange('Make')} on:edit={onEdit('Make')} />
  <ActionItem imgFlag={flag} title="机型" showSwitch data={option.Model} on:use-change={onUseChange('Model')} on:edit={onEdit('Model')} />
  <ActionItem imgFlag={flag} title="镜头厂商" showSwitch data={option.LensMake} on:use-change={onUseChange('LensMake')} on:edit={onEdit('LensMake')} />
  <ActionItem imgFlag={flag} title="镜头型号" showSwitch data={option.LensModel} on:use-change={onUseChange('LensModel')} on:edit={onEdit('LensModel')} />
  <ActionItem imgFlag={flag} title="光圈" showSwitch data={option.FNumber} on:use-change={onUseChange('FNumber')} on:edit={onEdit('FNumber')} />
  <ActionItem imgFlag={flag} title="焦距" showSwitch data={option.FocalLength} on:use-change={onUseChange('FocalLength')} on:edit={onEdit('FocalLength')} />
  <ActionItem imgFlag={flag} title="快门" showSwitch data={option.ExposureTime} on:use-change={onUseChange('ExposureTime')} on:edit={onEdit('ExposureTime')} />
  <ActionItem imgFlag={flag} title="ISO" showSwitch data={option.ISO} on:use-change={onUseChange('ISO')} on:edit={onEdit('ISO')} />
</Drawer>

<CustomParamDialog
  bind:visible={dialog.show}
  showImg={dialog.showImg}
  showType={dialog.showType}
  title={dialog.title}
  field={dialog.field}
  data={dialog.form}
  on:update={() => flag = Date.now()}
/>
