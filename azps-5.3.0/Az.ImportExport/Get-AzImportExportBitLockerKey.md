---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480277"
---
# <span data-ttu-id="75492-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="75492-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="75492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75492-102">SYNOPSIS</span></span>
<span data-ttu-id="75492-103">A megadott feladatban található összes meghajtó BitLocker-kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="75492-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="75492-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75492-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="75492-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75492-105">DESCRIPTION</span></span>
<span data-ttu-id="75492-106">A megadott feladatban található összes meghajtó BitLocker-kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="75492-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="75492-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75492-107">EXAMPLES</span></span>

### <span data-ttu-id="75492-108">1. példa: Az összes BitLocker-kulcs felsorolása a megadott ImportExport feladatban</span><span class="sxs-lookup"><span data-stu-id="75492-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="75492-109">Ez a parancsmag felsorolja a megadott ImportExport feladat összes BitLocker-kulcsát.</span><span class="sxs-lookup"><span data-stu-id="75492-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="75492-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75492-110">PARAMETERS</span></span>

### <span data-ttu-id="75492-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="75492-111">-AcceptLanguage</span></span>
<span data-ttu-id="75492-112">A válasz elsődleges nyelvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="75492-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75492-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75492-113">-DefaultProfile</span></span>
<span data-ttu-id="75492-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75492-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75492-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="75492-115">-JobName</span></span>
<span data-ttu-id="75492-116">Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="75492-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="75492-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75492-117">-ResourceGroupName</span></span>
<span data-ttu-id="75492-118">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="75492-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="75492-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75492-119">-SubscriptionId</span></span>
<span data-ttu-id="75492-120">Az Azure-felhasználó előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="75492-120">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75492-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75492-121">CommonParameters</span></span>
<span data-ttu-id="75492-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75492-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75492-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75492-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75492-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75492-124">INPUTS</span></span>

## <span data-ttu-id="75492-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75492-125">OUTPUTS</span></span>

### <span data-ttu-id="75492-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="75492-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="75492-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75492-127">NOTES</span></span>

<span data-ttu-id="75492-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="75492-128">ALIASES</span></span>

## <span data-ttu-id="75492-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75492-129">RELATED LINKS</span></span>

