<!DOCTYPE html>
<html>
    <head>        
        <script src="node_modules/frappe-gantt/dist/frappe-gantt.js"></script>
        <link rel="stylesheet" href="node_modules/frappe-gantt/dist/frappe-gantt.css">
        <link rel="stylesheet" href="cssAppPanini.css">
    </head>
    <body>
        <div class="cointainer">
            <div class="gantt-target">
            </div>
        </div>
        <script>//interpretato come java
            var tasks = [//array di oggetti(list)
            {
                    start: '2021-02-18',//attributo
                    end: '2021-02-25',
                    name: 'Analisi commessa',
                    id: 'task_0',
                    progress: 0,//percentuale
                },
                {
                    start: '2021-02-25',
                    end: '2021-02-26',
                    name: 'Definizione Budget',
                    id: 'task_1',
                    progress: 0,
                    dependencies: 'task_0'
                },
                { 
                    start: '2021-02-27',
                    end: '2021-03-6',
                    name: 'Progettazione concettuale',
                    id: 'task_2',
                    progress: 0,
                    dependencies: 'task_1'
                },
                {
                    start: '2021-03-6',
                    end: '2021-03-13',
                    name: 'Progettazione logica',
                    id: 'task_3',
                    progress: 0,
                    dependencies: 'task_2'
                },
                {
                    start: '2021-02-27',
                    end: '2021-03-10',
                    name: 'Pianificazione dell'infrastruttura della Rete',
                    id: 'task_4',
                    progress: 0,
                    dependencies: 'task_1'
                },
                {
                    start: '2021-02-27',
                    end: '2021-03-03',
                    name: 'Progettazione Sito Web',
                    id: 'task_5',
                    progress: 0,
                    dependencies: 'task_1'
                },
                {
                    start: '2021-03-13',
                    end: '2021-03-20',
                    name: 'Studio Della Concorrenza e Interviste',
                    id: 'task_6',
                    progress: 0,
                    dependencies: ['task_3','task_4', 'task_5']
                },
                {
                    start: '2021-03-10',
                    end: '2021-03-25',
                    name: 'Implementazione Rete',
                    id: 'task_7',
                    progress: 0,
                    dependencies: 'task_4'
                },
                {
                    start: '2021-03-03',
                    end: '2021-03-17',
                    name: 'Programmazione Sito Web',
                    id: 'task_8',
                    progress: 0,
                    dependencies: 'task_5'
                },
                    {
                    start: '2021-03-13',
                    end: '2021-03-27',
                    name: 'Progettazzione BataBase (Progettazione fisica e Popolazione)',
                    id: 'task_9',
                    progress: 0,
                    dependencies: 'task_3'
                },
                    {
                    start: '2021-03-27',
                    end: '2021-03-31',
                    name: 'Test di validazione e Collaudo',
                    id: 'task_10',
                    progress: 0,
                    dependencies: ['task_6','task_7', 'task_8', 'task_9']
                },
                    {
                    start: '2021-03-31',
                    end: '2021-04-05',
                    name: 'Installazione e avvio',
                    id: 'task_11',
                    progress: 0,
                    dependencies: 'task_10'
                }
            ]
            var gantt_char= new Gantt(".gantt-target", tasks,{
                view_modes:['Quarter Day','Half Day'],
                view_mode: 'Week',
                on_click: function(task){
                    console.log(task);
                    alert('ciao');
                },
            });//per vederlo           
        </script>
    </body>
</html>

