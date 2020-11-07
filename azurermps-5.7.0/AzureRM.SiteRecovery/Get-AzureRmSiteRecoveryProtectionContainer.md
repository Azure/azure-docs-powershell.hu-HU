---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: d5c2032828c5d34b94af8d448155c18b6d8b06c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679694"
---
# <span data-ttu-id="fb92c-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fb92c-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="fb92c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb92c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb92c-103">Védett tárolók a jelenlegi webhely-helyreállítási boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="fb92c-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb92c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb92c-104">SYNTAX</span></span>

### <span data-ttu-id="fb92c-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb92c-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb92c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fb92c-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb92c-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="fb92c-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb92c-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fb92c-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb92c-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="fb92c-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb92c-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="fb92c-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb92c-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb92c-111">DESCRIPTION</span></span>
<span data-ttu-id="fb92c-112">A **Get-AzureRmSiteRecoveryProtectionContainer** parancsmag védett tárolókat kap az aktuális Azure webhely-helyreállítási boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="fb92c-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="fb92c-113">A védelmi tároló egy logikai tároló a védett objektumokhoz, például a virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="fb92c-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="fb92c-114">A védelmi házirendek definiálják a védett elemek replikációs beállításait, és a védelemmel ellátott tárolóban használhatók, és egy védett entitásra alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="fb92c-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="fb92c-115">Példák</span><span class="sxs-lookup"><span data-stu-id="fb92c-115">EXAMPLES</span></span>

## <span data-ttu-id="fb92c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb92c-116">PARAMETERS</span></span>

### <span data-ttu-id="fb92c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb92c-117">-DefaultProfile</span></span>
<span data-ttu-id="fb92c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb92c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb92c-119">-Szövet</span><span class="sxs-lookup"><span data-stu-id="fb92c-119">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb92c-120">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="fb92c-120">-FriendlyName</span></span>
<span data-ttu-id="fb92c-121">A védelmi tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb92c-121">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb92c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb92c-122">-Name</span></span>
<span data-ttu-id="fb92c-123">A védelmi tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb92c-123">Specifies the name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb92c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb92c-124">CommonParameters</span></span>
<span data-ttu-id="fb92c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb92c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb92c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb92c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb92c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb92c-127">INPUTS</span></span>

### <span data-ttu-id="fb92c-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fb92c-128">ASRFabric</span></span>
<span data-ttu-id="fb92c-129">A "szövet" paraméter az "ASRFabric" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fb92c-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="fb92c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb92c-130">OUTPUTS</span></span>

### <span data-ttu-id="fb92c-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="fb92c-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="fb92c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb92c-132">NOTES</span></span>

## <span data-ttu-id="fb92c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb92c-133">RELATED LINKS</span></span>

