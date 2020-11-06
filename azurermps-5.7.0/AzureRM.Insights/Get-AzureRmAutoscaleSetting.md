---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 989CE245-FD1D-4E1D-90A2-2D7DA3975D0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleSetting.md
ms.openlocfilehash: fc503b135086fb698ae7be2f7318b0a5d63aafef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492274"
---
# <span data-ttu-id="8f7db-101">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8f7db-101">Get-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="8f7db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f7db-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7db-103">Az automéretarány beállításai.</span><span class="sxs-lookup"><span data-stu-id="8f7db-103">Gets Autoscale settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f7db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f7db-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleSetting -ResourceGroupName <String> [-Name <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f7db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f7db-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7db-106">A **Get-AzureRmAutoscaleSetting** parancsmag minden, az erőforráscsoport vagy a megadott automéretarány beállítással társított beállítást beolvassa.</span><span class="sxs-lookup"><span data-stu-id="8f7db-106">The **Get-AzureRmAutoscaleSetting** cmdlet gets all Autoscale settings associated with a resource group or a specified Autoscale setting.</span></span>

## <span data-ttu-id="8f7db-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8f7db-107">EXAMPLES</span></span>

### <span data-ttu-id="8f7db-108">1. példa: az időskála beállításainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="8f7db-108">Example 1: Get Autoscale settings</span></span>
```
PS C:\>Get-AzureRmAutoscaleSetting -ResourceGroup "Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction        : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction  : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1

MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
                                                TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
                                                Direction  : Increase
Type       : ChangeCount
Value      : 1
             TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="8f7db-109">Ez a parancs beolvassa az alapértelmezett erőforráscsoport-webhelyhez rendelt automatikus méretezési beállításokat a EastUS.</span><span class="sxs-lookup"><span data-stu-id="8f7db-109">This command gets the Autoscale settings assigned to the resource group Default-Web-EastUS.</span></span>

### <span data-ttu-id="8f7db-110">2. példa: az automéretarány beállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="8f7db-110">Example 2: Get an Autoscale setting by name</span></span>
```
PS C:\>Get-AzureRmAutoscaleSetting -ResourceGroupName "Default-Web-EastUS" -Name "DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="8f7db-111">Ez a parancs a DefaultServerFarm-Default-Web-EastUS nevű automatikus méretezési beállítást kapja.</span><span class="sxs-lookup"><span data-stu-id="8f7db-111">This command gets the Autoscale setting named DefaultServerFarm-Default-Web-EastUS.</span></span>

## <span data-ttu-id="8f7db-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f7db-112">PARAMETERS</span></span>

### <span data-ttu-id="8f7db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7db-113">-DefaultProfile</span></span>
<span data-ttu-id="8f7db-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8f7db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7db-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="8f7db-115">-DetailedOutput</span></span>
<span data-ttu-id="8f7db-116">Jelzi, hogy a művelet minden részletet megjelenít a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="8f7db-116">Indicates that this operation displays full details in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7db-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f7db-117">-Name</span></span>
<span data-ttu-id="8f7db-118">A beolvasott beállítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f7db-118">Specifies the name of the setting to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7db-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f7db-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f7db-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7db-121">CommonParameters</span></span>
<span data-ttu-id="8f7db-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f7db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7db-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7db-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7db-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f7db-124">INPUTS</span></span>

### <span data-ttu-id="8f7db-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="8f7db-125">None</span></span>
<span data-ttu-id="8f7db-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8f7db-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f7db-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f7db-127">OUTPUTS</span></span>

### <span data-ttu-id="8f7db-128">Lista<PSAutoscaleSetting></span><span class="sxs-lookup"><span data-stu-id="8f7db-128">List<PSAutoscaleSetting></span></span>

## <span data-ttu-id="8f7db-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f7db-129">NOTES</span></span>

## <span data-ttu-id="8f7db-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f7db-130">RELATED LINKS</span></span>

[<span data-ttu-id="8f7db-131">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8f7db-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="8f7db-132">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8f7db-132">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


