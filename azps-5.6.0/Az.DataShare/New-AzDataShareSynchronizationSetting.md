---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 5632aed8c1b3dde653be65fd587be5f1adf9cbbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941842"
---
# <span data-ttu-id="7e300-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="7e300-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="7e300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e300-102">SYNOPSIS</span></span>
<span data-ttu-id="7e300-103">Szinkronizálási beállítást hoz létre egy megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="7e300-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="7e300-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e300-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e300-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e300-105">DESCRIPTION</span></span>
<span data-ttu-id="7e300-106">A **New-AzDataShareSynchronizationSetting** létrehoz egy szinkronizálási beállítást a megosztási fiókban, amely akár naponta, akár óránként ismétlődik egy adott időpontban.</span><span class="sxs-lookup"><span data-stu-id="7e300-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="7e300-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e300-107">EXAMPLES</span></span>

### <span data-ttu-id="7e300-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7e300-108">Example 1</span></span>
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

<span data-ttu-id="7e300-109">Ez a parancs szinkronizálási beállítást hoz létre napi ismétlődési intervallumon, 9:00 órakor a AdsShare megosztásához a WikiAds adatmegosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="7e300-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="7e300-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e300-110">PARAMETERS</span></span>

### <span data-ttu-id="7e300-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e300-111">-AccountName</span></span>
<span data-ttu-id="7e300-112">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="7e300-112">Azure data share account name</span></span>

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

### <span data-ttu-id="7e300-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e300-113">-DefaultProfile</span></span>
<span data-ttu-id="7e300-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e300-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e300-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7e300-115">-Name</span></span>
<span data-ttu-id="7e300-116">Szinkronizálási beállítás neve</span><span class="sxs-lookup"><span data-stu-id="7e300-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="7e300-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="7e300-117">-RecurrenceInterval</span></span>
<span data-ttu-id="7e300-118">A szinkronizálási beállítás ismétlődési időköze (nap vagy óra)</span><span class="sxs-lookup"><span data-stu-id="7e300-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="7e300-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e300-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e300-120">Az Azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="7e300-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="7e300-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7e300-121">-ShareName</span></span>
<span data-ttu-id="7e300-122">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="7e300-122">Azure data share name</span></span>

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

### <span data-ttu-id="7e300-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="7e300-123">-SynchronizationTime</span></span>
<span data-ttu-id="7e300-124">Az ütemezett szinkronizálási beállítás kezdési ideje</span><span class="sxs-lookup"><span data-stu-id="7e300-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="7e300-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e300-125">-Confirm</span></span>
<span data-ttu-id="7e300-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7e300-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e300-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e300-127">-WhatIf</span></span>
<span data-ttu-id="7e300-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7e300-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e300-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e300-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e300-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e300-130">CommonParameters</span></span>
<span data-ttu-id="7e300-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e300-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e300-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e300-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e300-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e300-133">INPUTS</span></span>

### <span data-ttu-id="7e300-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="7e300-134">None</span></span>

## <span data-ttu-id="7e300-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e300-135">OUTPUTS</span></span>

### <span data-ttu-id="7e300-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="7e300-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="7e300-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e300-137">NOTES</span></span>

## <span data-ttu-id="7e300-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e300-138">RELATED LINKS</span></span>
