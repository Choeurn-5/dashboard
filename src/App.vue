<template>
  <div class="dashboard bg-gray-100 min-h-screen p-6">
    <Header />

    <div class="grid grid-cols-4 gap-4 mt-6">
      <CardProgress
        title="ឯកសារចូលពីក្រសួងអង្គភាពក្រុមចំរុះ"
        :progressData="progressCards[0].data"
      />
      <CardProgress
        title="ឯកសាចូលពីក្រសួងស្ថាប័ន"
        :progressData="progressCards[1].data"
      />
      <!-- <SummaryCard
        title="សង្ខេប"
        :summaryData="summaryData"
      /> -->
    <div>
      <NotificationItem />
      <NotificationItem />
    </div>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import CardProgress from './components/CardProgress.vue';
import SummaryCard from './components/SummaryCard.vue';
import NotificationItem from './components/NotificationItem.vue';

export default {
  components: {
    Header,
    CardProgress,
    SummaryCard,
    NotificationItem
  },
  data() {
    return {
      progressCards: [
        { data: [{ label: 'នាយកដ្ឋានរដ្ឋបាលសរុប', value: 50 }, { label: 'អគ្គស្នងការនគបាលជាតិ', value: 80 }] },
        { data: [{ label: 'ក្រសួងការបរទេស', value: 30 }, { label: 'ក្រសួងសេដ្ឋកិច្ចហិរញ្ញវត្ថុ', value: 70 }] },
        { data: [{ label: 'ក្រសួង', value: 30 }, { label: 'ក្រសួងសេដ្ឋកិច្ចហិរញ្ញវត្ថុ', value: 70 }] }

        
      ],
      summaryData: [
        { id: 1, icon: '📄', text: 'Item 1' },
        { id: 2, icon: '📄', text: 'Item 2' }
     
      ]
    };
  }
};
</script>
