<script>
import BaseComponent from 'primevue/basecomponent';
import SidebarStyle from 'primevue/sidebar/style';

export default {
    name: 'BaseSidebar',
    extends: BaseComponent,
    props: {
        visible: {
            type: Boolean,
            default: false
        },
        position: {
            type: String,
            default: 'left'
        },
        baseZIndex: {
            type: Number,
            default: 0
        },
        autoZIndex: {
            type: Boolean,
            default: true
        },
        dismissable: {
            type: Boolean,
            default: true
        },
        showCloseIcon: {
            type: Boolean,
            default: true
        },
        closeIcon: {
            type: String,
            default: undefined
        },
        modal: {
            type: Boolean,
            default: true
        },
        blockScroll: {
            type: Boolean,
            default: false
        }
    },
    style: SidebarStyle,
    provide() {
        return {
            $parentInstance: this
        };
    }
};
</script>
