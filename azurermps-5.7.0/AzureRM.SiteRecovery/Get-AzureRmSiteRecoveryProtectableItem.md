---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 2a857c538188c2b9ddf7516ccebda291f3161e1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502411"
---
# <span data-ttu-id="3ae42-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3ae42-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="3ae42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ae42-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae42-103">A védelemmel ellátott elemek beolvasása egy védelmi tárolóban</span><span class="sxs-lookup"><span data-stu-id="3ae42-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ae42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ae42-104">SYNTAX</span></span>

### <span data-ttu-id="3ae42-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ae42-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ae42-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3ae42-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ae42-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3ae42-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ae42-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ae42-108">DESCRIPTION</span></span>
<span data-ttu-id="3ae42-109">A **Get-AzureRmSiteRecoveryProtectableItem** parancsmag az Azure webhely-helyreállítási védelmi tárolóban található védelemmel ellátott elemeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3ae42-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="3ae42-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ae42-110">EXAMPLES</span></span>

## <span data-ttu-id="3ae42-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ae42-111">PARAMETERS</span></span>

### <span data-ttu-id="3ae42-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae42-112">-DefaultProfile</span></span>
<span data-ttu-id="3ae42-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ae42-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ae42-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="3ae42-114">-FriendlyName</span></span>
<span data-ttu-id="3ae42-115">Megadja az Azure webhely-helyreállítási elem rövid nevét.</span><span class="sxs-lookup"><span data-stu-id="3ae42-115">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae42-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ae42-116">-Name</span></span>
<span data-ttu-id="3ae42-117">Az Azure webhely-helyreállítási védelemmel ellátott elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ae42-117">Specifies the name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae42-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3ae42-118">-ProtectionContainer</span></span>
<span data-ttu-id="3ae42-119">Az Azure site Recovery Protection Container objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ae42-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ae42-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae42-120">CommonParameters</span></span>
<span data-ttu-id="3ae42-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ae42-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae42-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ae42-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae42-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ae42-123">INPUTS</span></span>

### <span data-ttu-id="3ae42-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3ae42-124">ASRProtectionContainer</span></span>
<span data-ttu-id="3ae42-125">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3ae42-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="3ae42-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ae42-126">OUTPUTS</span></span>

### <span data-ttu-id="3ae42-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3ae42-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3ae42-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ae42-128">NOTES</span></span>

## <span data-ttu-id="3ae42-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ae42-129">RELATED LINKS</span></span>

[<span data-ttu-id="3ae42-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3ae42-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="3ae42-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3ae42-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
