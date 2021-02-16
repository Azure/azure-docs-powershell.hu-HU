---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: df8f61b10750f50bef1b3417da7f28be4ec0d0d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161818"
---
# <span data-ttu-id="93aa0-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="93aa0-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="93aa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="93aa0-103">Szinkronizálási beállítást hoz létre egy megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="93aa0-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="93aa0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93aa0-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93aa0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93aa0-105">DESCRIPTION</span></span>
<span data-ttu-id="93aa0-106">A **New-AzDataShareSynchronizationSetting** létrehoz egy szinkronizálási beállítást a megosztási fiókban való megosztáshoz, amely akár naponta, akár óránként ismétlődik egy adott időpontban.</span><span class="sxs-lookup"><span data-stu-id="93aa0-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="93aa0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93aa0-107">EXAMPLES</span></span>

### <span data-ttu-id="93aa0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="93aa0-108">Example 1</span></span>
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

<span data-ttu-id="93aa0-109">Ez a parancs szinkronizálási beállítást hoz létre napi ismétlődési intervallumon, 9:00 órakor a AdsShare megosztásához a WikiAds adatmegosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="93aa0-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="93aa0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93aa0-110">PARAMETERS</span></span>

### <span data-ttu-id="93aa0-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="93aa0-111">-AccountName</span></span>
<span data-ttu-id="93aa0-112">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="93aa0-112">Azure data share account name</span></span>

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

### <span data-ttu-id="93aa0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93aa0-113">-DefaultProfile</span></span>
<span data-ttu-id="93aa0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93aa0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93aa0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="93aa0-115">-Name</span></span>
<span data-ttu-id="93aa0-116">Szinkronizálási beállítás neve</span><span class="sxs-lookup"><span data-stu-id="93aa0-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="93aa0-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="93aa0-117">-RecurrenceInterval</span></span>
<span data-ttu-id="93aa0-118">A szinkronizálási beállítás ismétlődési időköze (nap vagy óra)</span><span class="sxs-lookup"><span data-stu-id="93aa0-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="93aa0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93aa0-119">-ResourceGroupName</span></span>
<span data-ttu-id="93aa0-120">Az Azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="93aa0-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="93aa0-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="93aa0-121">-ShareName</span></span>
<span data-ttu-id="93aa0-122">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="93aa0-122">Azure data share name</span></span>

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

### <span data-ttu-id="93aa0-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="93aa0-123">-SynchronizationTime</span></span>
<span data-ttu-id="93aa0-124">Az ütemezett szinkronizálási beállítás kezdési ideje</span><span class="sxs-lookup"><span data-stu-id="93aa0-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="93aa0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93aa0-125">-Confirm</span></span>
<span data-ttu-id="93aa0-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="93aa0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93aa0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93aa0-127">-WhatIf</span></span>
<span data-ttu-id="93aa0-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="93aa0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93aa0-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93aa0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93aa0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93aa0-130">CommonParameters</span></span>
<span data-ttu-id="93aa0-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93aa0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93aa0-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93aa0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93aa0-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93aa0-133">INPUTS</span></span>

### <span data-ttu-id="93aa0-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="93aa0-134">None</span></span>

## <span data-ttu-id="93aa0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93aa0-135">OUTPUTS</span></span>

### <span data-ttu-id="93aa0-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="93aa0-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="93aa0-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93aa0-137">NOTES</span></span>

## <span data-ttu-id="93aa0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93aa0-138">RELATED LINKS</span></span>
