---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: a10f7ffb1b05474e5d2b86fa7d7a55f825aaad25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680503"
---
# <span data-ttu-id="def2e-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="def2e-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="def2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="def2e-102">SYNOPSIS</span></span>
<span data-ttu-id="def2e-103">Helyreállítási terv vagy az összes helyreállítási csomag beszerzése a helyreállítási szolgáltatások pincéjében</span><span class="sxs-lookup"><span data-stu-id="def2e-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="def2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="def2e-104">SYNTAX</span></span>

### <span data-ttu-id="def2e-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="def2e-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [<CommonParameters>]
```

### <span data-ttu-id="def2e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="def2e-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>] [<CommonParameters>]
```

### <span data-ttu-id="def2e-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="def2e-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>] [<CommonParameters>]
```

## <span data-ttu-id="def2e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="def2e-108">DESCRIPTION</span></span>
<span data-ttu-id="def2e-109">A **Get-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag a helyreállítási szolgáltatások pincéjében megadott helyreállítási terv vagy minden helyreállítási csomag részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="def2e-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="def2e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="def2e-110">EXAMPLES</span></span>

### <span data-ttu-id="def2e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="def2e-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="def2e-112">A megadott nevű helyreállítási csomagot kapja.</span><span class="sxs-lookup"><span data-stu-id="def2e-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="def2e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="def2e-113">PARAMETERS</span></span>

### <span data-ttu-id="def2e-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="def2e-114">-FriendlyName</span></span>
<span data-ttu-id="def2e-115">A beolvasott helyreállítási terv rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="def2e-115">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def2e-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="def2e-116">-Name</span></span>
<span data-ttu-id="def2e-117">A beolvasott helyreállítási terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="def2e-117">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def2e-118">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="def2e-118">-Path</span></span>
<span data-ttu-id="def2e-119">Annak a fájlnak az elérési útvonalát adja meg, amelybe a parancsmag a helyreállítási terv JSON-definícióját menti.</span><span class="sxs-lookup"><span data-stu-id="def2e-119">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="def2e-120">A JSON-definíció szerkeszthető a helyreállítási terv módosításához és a helyreállítási terv Update-AzureRmRecoveryServicesASRRecoveryPlan parancsmagon keresztüli frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="def2e-120">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def2e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def2e-121">CommonParameters</span></span>
<span data-ttu-id="def2e-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="def2e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def2e-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def2e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def2e-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="def2e-124">INPUTS</span></span>

### <span data-ttu-id="def2e-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="def2e-125">None</span></span>

## <span data-ttu-id="def2e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="def2e-126">OUTPUTS</span></span>

### <span data-ttu-id="def2e-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="def2e-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="def2e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="def2e-128">NOTES</span></span>

## <span data-ttu-id="def2e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="def2e-129">RELATED LINKS</span></span>

[<span data-ttu-id="def2e-130">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="def2e-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="def2e-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="def2e-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="def2e-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="def2e-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
