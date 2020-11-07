---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 9601a3a9a64e52938ebad2024bbc9fd1301b920a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680221"
---
# <span data-ttu-id="abd2c-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="abd2c-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="abd2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="abd2c-103">Azure-webhely-helyreállítási szövetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="abd2c-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abd2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abd2c-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abd2c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="abd2c-105">DESCRIPTION</span></span>
<span data-ttu-id="abd2c-106">A **New-AzureRmSiteRecoveryFabric** parancsmag a megadott típusú Azure webhely-helyreállítási szerkezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="abd2c-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="abd2c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="abd2c-107">EXAMPLES</span></span>

## <span data-ttu-id="abd2c-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abd2c-108">PARAMETERS</span></span>

### <span data-ttu-id="abd2c-109">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abd2c-109">-Name</span></span>
<span data-ttu-id="abd2c-110">Az Azure webhely-helyreállítási anyag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abd2c-110">Specifies the name of the Azure Site Recovery Fabric</span></span>

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

### <span data-ttu-id="abd2c-111">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="abd2c-111">-Type</span></span>
<span data-ttu-id="abd2c-112">Az Azure webhely-helyreállítási anyag típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="abd2c-112">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd2c-113">-DefaultProfile</span></span>
<span data-ttu-id="abd2c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abd2c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abd2c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd2c-115">CommonParameters</span></span>
<span data-ttu-id="abd2c-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abd2c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd2c-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd2c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd2c-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd2c-118">INPUTS</span></span>

## <span data-ttu-id="abd2c-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd2c-119">OUTPUTS</span></span>

### <span data-ttu-id="abd2c-120">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="abd2c-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="abd2c-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abd2c-121">NOTES</span></span>

## <span data-ttu-id="abd2c-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abd2c-122">RELATED LINKS</span></span>

[<span data-ttu-id="abd2c-123">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="abd2c-123">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="abd2c-124">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="abd2c-124">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
