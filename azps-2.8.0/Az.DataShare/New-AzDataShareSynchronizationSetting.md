---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: ba8f51832aada036363dea95a8f604b24966e76b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666702"
---
# <span data-ttu-id="96413-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="96413-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="96413-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96413-102">SYNOPSIS</span></span>
<span data-ttu-id="96413-103">Szinkronizálási beállítást hoz létre a megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="96413-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="96413-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96413-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96413-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96413-105">DESCRIPTION</span></span>
<span data-ttu-id="96413-106">A **AzDataShareSynchronizationSetting** létrehoz egy szinkronizálási beállítást a megosztási fiók megosztási fiókjában, amely egy adott időpontban naponta vagy óránként megismétlődik.</span><span class="sxs-lookup"><span data-stu-id="96413-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="96413-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96413-107">EXAMPLES</span></span>

### <span data-ttu-id="96413-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="96413-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="96413-109">A parancsok szinkronizálási beállítást hoz létre a napi ismétlődési időintervallumban a 9:00-ban az adatmegosztási fiók WikiAds AdsShare megosztásához.</span><span class="sxs-lookup"><span data-stu-id="96413-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="96413-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96413-110">PARAMETERS</span></span>

### <span data-ttu-id="96413-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96413-111">-AccountName</span></span>
<span data-ttu-id="96413-112">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="96413-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96413-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96413-113">-DefaultProfile</span></span>
<span data-ttu-id="96413-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96413-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96413-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96413-115">-Name</span></span>
<span data-ttu-id="96413-116">Szinkronizálási beállítás neve</span><span class="sxs-lookup"><span data-stu-id="96413-116">Synchronization setting name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96413-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="96413-117">-RecurrenceInterval</span></span>
<span data-ttu-id="96413-118">A szinkronizálási beállítás ismétlődési intervalluma (nap vagy óra)</span><span class="sxs-lookup"><span data-stu-id="96413-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96413-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96413-119">-ResourceGroupName</span></span>
<span data-ttu-id="96413-120">Az Azure Data Share-fiók erőforrás-csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="96413-120">Resource group name of azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96413-121">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="96413-121">-ShareName</span></span>
<span data-ttu-id="96413-122">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="96413-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96413-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="96413-123">-SynchronizationTime</span></span>
<span data-ttu-id="96413-124">Az ütemezett szinkronizálási beállítás kezdési időpontja</span><span class="sxs-lookup"><span data-stu-id="96413-124">The start time of the scheduled synchronization setting</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96413-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96413-125">-Confirm</span></span>
<span data-ttu-id="96413-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96413-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96413-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96413-127">-WhatIf</span></span>
<span data-ttu-id="96413-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96413-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96413-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96413-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96413-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96413-130">CommonParameters</span></span>
<span data-ttu-id="96413-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96413-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96413-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96413-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96413-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96413-133">INPUTS</span></span>

### <span data-ttu-id="96413-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="96413-134">None</span></span>

## <span data-ttu-id="96413-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96413-135">OUTPUTS</span></span>

### <span data-ttu-id="96413-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="96413-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="96413-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96413-137">NOTES</span></span>

## <span data-ttu-id="96413-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96413-138">RELATED LINKS</span></span>
