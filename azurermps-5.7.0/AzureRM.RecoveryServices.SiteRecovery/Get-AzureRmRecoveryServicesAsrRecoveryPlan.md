---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b95c3ab14d50558ef184beabcd461a59bb1a05ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494407"
---
# <span data-ttu-id="eb93b-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb93b-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="eb93b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb93b-102">SYNOPSIS</span></span>
<span data-ttu-id="eb93b-103">Helyreállítási terv vagy az összes helyreállítási csomag beszerzése a helyreállítási szolgáltatások pincéjében</span><span class="sxs-lookup"><span data-stu-id="eb93b-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb93b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb93b-104">SYNTAX</span></span>

### <span data-ttu-id="eb93b-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb93b-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb93b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="eb93b-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb93b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="eb93b-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb93b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb93b-108">DESCRIPTION</span></span>
<span data-ttu-id="eb93b-109">A **Get-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag a helyreállítási szolgáltatások pincéjében megadott helyreállítási terv vagy minden helyreállítási csomag részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eb93b-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="eb93b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eb93b-110">EXAMPLES</span></span>

### <span data-ttu-id="eb93b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb93b-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="eb93b-112">A megadott nevű helyreállítási csomagot kapja.</span><span class="sxs-lookup"><span data-stu-id="eb93b-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="eb93b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb93b-113">PARAMETERS</span></span>

### <span data-ttu-id="eb93b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb93b-114">-DefaultProfile</span></span>
<span data-ttu-id="eb93b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb93b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="eb93b-116">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="eb93b-116">-FriendlyName</span></span>
<span data-ttu-id="eb93b-117">A beolvasott helyreállítási terv rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb93b-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="eb93b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb93b-118">-Name</span></span>
<span data-ttu-id="eb93b-119">A beolvasott helyreállítási terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb93b-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="eb93b-120">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="eb93b-120">-Path</span></span>
<span data-ttu-id="eb93b-121">Annak a fájlnak az elérési útvonalát adja meg, amelybe a parancsmag a helyreállítási terv JSON-definícióját menti.</span><span class="sxs-lookup"><span data-stu-id="eb93b-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="eb93b-122">A JSON-definíció szerkeszthető a helyreállítási terv módosításához és a helyreállítási terv Update-AzureRmRecoveryServicesASRRecoveryPlan parancsmagon keresztüli frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="eb93b-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="eb93b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb93b-123">CommonParameters</span></span>
<span data-ttu-id="eb93b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb93b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb93b-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb93b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb93b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb93b-126">INPUTS</span></span>

### <span data-ttu-id="eb93b-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="eb93b-127">None</span></span>

## <span data-ttu-id="eb93b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb93b-128">OUTPUTS</span></span>

### <span data-ttu-id="eb93b-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eb93b-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="eb93b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb93b-130">NOTES</span></span>

## <span data-ttu-id="eb93b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb93b-131">RELATED LINKS</span></span>

[<span data-ttu-id="eb93b-132">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb93b-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="eb93b-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb93b-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="eb93b-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb93b-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
