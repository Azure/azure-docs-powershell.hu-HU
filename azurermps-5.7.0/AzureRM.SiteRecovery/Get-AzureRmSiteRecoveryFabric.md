---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 63d28696370f5219a4c2a21c6fb3097441a11433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498784"
---
# <span data-ttu-id="e8831-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="e8831-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="e8831-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8831-102">SYNOPSIS</span></span>
<span data-ttu-id="e8831-103">Az Azure webhely-helyreállítási anyag tulajdonságainak beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e8831-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8831-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8831-104">SYNTAX</span></span>

### <span data-ttu-id="e8831-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8831-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8831-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e8831-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8831-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e8831-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8831-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8831-108">DESCRIPTION</span></span>
<span data-ttu-id="e8831-109">A **Get-AzureRmSiteRecoveryFabric** parancsmag egy megadott Azure-webhely helyreállítási szövetének vagy minden Azure webhely-helyreállítási szövetnek a tulajdonságait adja meg helyreállítási szolgáltatás-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="e8831-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="e8831-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e8831-110">EXAMPLES</span></span>

## <span data-ttu-id="e8831-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8831-111">PARAMETERS</span></span>

### <span data-ttu-id="e8831-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8831-112">-DefaultProfile</span></span>
<span data-ttu-id="e8831-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8831-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8831-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="e8831-114">-FriendlyName</span></span>
<span data-ttu-id="e8831-115">Az Azure webhely-helyreállítási anyag rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8831-115">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="e8831-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8831-116">-Name</span></span>
<span data-ttu-id="e8831-117">Az Azure webhely-helyreállítási anyag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8831-117">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="e8831-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8831-118">CommonParameters</span></span>
<span data-ttu-id="e8831-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8831-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8831-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8831-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8831-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8831-121">INPUTS</span></span>

### <span data-ttu-id="e8831-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="e8831-122">None</span></span>
<span data-ttu-id="e8831-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e8831-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8831-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8831-124">OUTPUTS</span></span>

### <span data-ttu-id="e8831-125">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRFabric, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e8831-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e8831-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8831-126">NOTES</span></span>

## <span data-ttu-id="e8831-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8831-127">RELATED LINKS</span></span>

[<span data-ttu-id="e8831-128">Új – AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="e8831-128">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="e8831-129">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="e8831-129">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
