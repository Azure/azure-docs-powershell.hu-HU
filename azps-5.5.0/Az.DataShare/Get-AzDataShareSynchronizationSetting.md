---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148059"
---
# <span data-ttu-id="e980d-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="e980d-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="e980d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e980d-102">SYNOPSIS</span></span>
<span data-ttu-id="e980d-103">Információkat kap a megosztáson beállított szinkronizálásról.</span><span class="sxs-lookup"><span data-stu-id="e980d-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="e980d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e980d-104">SYNTAX</span></span>

### <span data-ttu-id="e980d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e980d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e980d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e980d-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e980d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e980d-107">DESCRIPTION</span></span>
<span data-ttu-id="e980d-108">A **Get-AzDataShareSynchronizationSetting** parancsmag információt nyújt a megosztáson engedélyezett szinkronizálásról.</span><span class="sxs-lookup"><span data-stu-id="e980d-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="e980d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e980d-109">EXAMPLES</span></span>

### <span data-ttu-id="e980d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e980d-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="e980d-111">Ez a parancs információkat nyújt a ShareSynchronization szinkronizálásról, amely engedélyezve van a ShareShare-megosztáson a WikiAds adatmegosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="e980d-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="e980d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e980d-112">PARAMETERS</span></span>

### <span data-ttu-id="e980d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e980d-113">-AccountName</span></span>
<span data-ttu-id="e980d-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="e980d-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e980d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e980d-115">-DefaultProfile</span></span>
<span data-ttu-id="e980d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e980d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e980d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e980d-117">-Name</span></span>
<span data-ttu-id="e980d-118">Szinkronizálási beállítás neve</span><span class="sxs-lookup"><span data-stu-id="e980d-118">Name for Synchronization Setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e980d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e980d-119">-ResourceGroupName</span></span>
<span data-ttu-id="e980d-120">Az Azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="e980d-120">Resource group name of azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e980d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e980d-121">-ResourceId</span></span>
<span data-ttu-id="e980d-122">Az Azure-adatok megosztására vonatkozó szinkronizálási beállítás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e980d-122">The resource id of the azure data share synchronization setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e980d-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e980d-123">-ShareName</span></span>
<span data-ttu-id="e980d-124">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="e980d-124">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e980d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e980d-125">CommonParameters</span></span>
<span data-ttu-id="e980d-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e980d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e980d-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e980d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e980d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e980d-128">INPUTS</span></span>

### <span data-ttu-id="e980d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e980d-129">System.String</span></span>

## <span data-ttu-id="e980d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e980d-130">OUTPUTS</span></span>

### <span data-ttu-id="e980d-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="e980d-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="e980d-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e980d-132">NOTES</span></span>

## <span data-ttu-id="e980d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e980d-133">RELATED LINKS</span></span>
