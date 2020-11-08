---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182751"
---
# <span data-ttu-id="7d46f-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="7d46f-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="7d46f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d46f-102">SYNOPSIS</span></span>
<span data-ttu-id="7d46f-103">A megadott feladat összes meghajtójának BitLocker-kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7d46f-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="7d46f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d46f-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7d46f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d46f-105">DESCRIPTION</span></span>
<span data-ttu-id="7d46f-106">A megadott feladat összes meghajtójának BitLocker-kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7d46f-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="7d46f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7d46f-107">EXAMPLES</span></span>

### <span data-ttu-id="7d46f-108">Példa 1: az összes BitLocker-kulcs listázása a megadott ImportExport-projektben</span><span class="sxs-lookup"><span data-stu-id="7d46f-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="7d46f-109">Ez a parancsmag a megadott ImportExport-feladat összes BitLocker-kulcsát megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="7d46f-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="7d46f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d46f-110">PARAMETERS</span></span>

### <span data-ttu-id="7d46f-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="7d46f-111">-AcceptLanguage</span></span>
<span data-ttu-id="7d46f-112">A válasz kívánt nyelvét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d46f-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="7d46f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d46f-113">-DefaultProfile</span></span>
<span data-ttu-id="7d46f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d46f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d46f-115">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="7d46f-115">-JobName</span></span>
<span data-ttu-id="7d46f-116">Az Importálás/exportálás feladat neve.</span><span class="sxs-lookup"><span data-stu-id="7d46f-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="7d46f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d46f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d46f-118">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="7d46f-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="7d46f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d46f-119">-SubscriptionId</span></span>
<span data-ttu-id="7d46f-120">Az Azure-felhasználó előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7d46f-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="7d46f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d46f-121">CommonParameters</span></span>
<span data-ttu-id="7d46f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d46f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d46f-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7d46f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d46f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d46f-124">INPUTS</span></span>

## <span data-ttu-id="7d46f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d46f-125">OUTPUTS</span></span>

### <span data-ttu-id="7d46f-126">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. modellek. Api20161101. IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="7d46f-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="7d46f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d46f-127">NOTES</span></span>

<span data-ttu-id="7d46f-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7d46f-128">ALIASES</span></span>

## <span data-ttu-id="7d46f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d46f-129">RELATED LINKS</span></span>

