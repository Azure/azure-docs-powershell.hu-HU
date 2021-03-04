---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: a4d3adbcc63eda80bced31523a43cbbad4513205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938186"
---
# <span data-ttu-id="794f3-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="794f3-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="794f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="794f3-102">SYNOPSIS</span></span>
<span data-ttu-id="794f3-103">Információkat kap a megosztás szinkronizálási beállításával kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="794f3-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="794f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="794f3-104">SYNTAX</span></span>

### <span data-ttu-id="794f3-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="794f3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="794f3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="794f3-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="794f3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="794f3-107">DESCRIPTION</span></span>
<span data-ttu-id="794f3-108">A **Get-AzDataShareSynchronization** parancsmag információt nyújt az adatmegosztási fiókban egy megosztásban szereplő összes szinkronizálási beállításról.</span><span class="sxs-lookup"><span data-stu-id="794f3-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="794f3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="794f3-109">EXAMPLES</span></span>

### <span data-ttu-id="794f3-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="794f3-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="794f3-111">Ez a parancs információt nyújt a Share AdsShare szolgáltatásban a WikiAds adatmegosztási fiókban található összes szinkronizálási beállításról.</span><span class="sxs-lookup"><span data-stu-id="794f3-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="794f3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="794f3-112">PARAMETERS</span></span>

### <span data-ttu-id="794f3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="794f3-113">-AccountName</span></span>
<span data-ttu-id="794f3-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="794f3-114">Azure data share account name</span></span>

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

### <span data-ttu-id="794f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="794f3-115">-DefaultProfile</span></span>
<span data-ttu-id="794f3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="794f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="794f3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="794f3-117">-ResourceGroupName</span></span>
<span data-ttu-id="794f3-118">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="794f3-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="794f3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="794f3-119">-ResourceId</span></span>
<span data-ttu-id="794f3-120">Azure-adatok megosztása erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="794f3-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="794f3-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="794f3-121">-ShareName</span></span>
<span data-ttu-id="794f3-122">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="794f3-122">Azure data share name</span></span>

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

### <span data-ttu-id="794f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794f3-123">CommonParameters</span></span>
<span data-ttu-id="794f3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="794f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794f3-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="794f3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794f3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="794f3-126">INPUTS</span></span>

### <span data-ttu-id="794f3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="794f3-127">System.String</span></span>

## <span data-ttu-id="794f3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="794f3-128">OUTPUTS</span></span>

### <span data-ttu-id="794f3-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="794f3-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="794f3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="794f3-130">NOTES</span></span>

## <span data-ttu-id="794f3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="794f3-131">RELATED LINKS</span></span>
