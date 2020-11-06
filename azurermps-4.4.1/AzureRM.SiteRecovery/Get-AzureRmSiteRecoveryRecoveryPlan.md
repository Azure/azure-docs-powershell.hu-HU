---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 2d9f087b87d99003b559fc363265fdb4b996c3f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494649"
---
# <span data-ttu-id="4fbbc-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fbbc-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="4fbbc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbbc-103">Helyreállítási csomagot kap a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="4fbbc-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fbbc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fbbc-104">SYNTAX</span></span>

### <span data-ttu-id="4fbbc-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fbbc-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fbbc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4fbbc-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fbbc-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4fbbc-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fbbc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fbbc-108">DESCRIPTION</span></span>
<span data-ttu-id="4fbbc-109">A **Get-AzureRmSiteRecoveryRecoveryPlan** parancsmag helyreállítási csomagot kap az Azure webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="4fbbc-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="4fbbc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4fbbc-110">EXAMPLES</span></span>

## <span data-ttu-id="4fbbc-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fbbc-111">PARAMETERS</span></span>

### <span data-ttu-id="4fbbc-112">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="4fbbc-112">-FriendlyName</span></span>
<span data-ttu-id="4fbbc-113">Annak a helyreállítási tervnek a rövid nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4fbbc-113">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbbc-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fbbc-114">-Name</span></span>
<span data-ttu-id="4fbbc-115">Annak a helyreállítási tervnek a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4fbbc-115">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbbc-116">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="4fbbc-116">-Path</span></span>
<span data-ttu-id="4fbbc-117">Annak a fájlnak az elérési útját adja meg, amelyre a parancsmag menti a helyreállítási csomagot.</span><span class="sxs-lookup"><span data-stu-id="4fbbc-117">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbbc-118">-DefaultProfile</span></span>
<span data-ttu-id="4fbbc-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fbbc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbbc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbbc-120">CommonParameters</span></span>
<span data-ttu-id="4fbbc-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fbbc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbbc-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fbbc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbbc-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fbbc-123">INPUTS</span></span>

## <span data-ttu-id="4fbbc-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fbbc-124">OUTPUTS</span></span>

### <span data-ttu-id="4fbbc-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="4fbbc-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="4fbbc-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fbbc-126">NOTES</span></span>

## <span data-ttu-id="4fbbc-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fbbc-127">RELATED LINKS</span></span>

[<span data-ttu-id="4fbbc-128">Új – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fbbc-128">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4fbbc-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fbbc-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4fbbc-130">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fbbc-130">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
