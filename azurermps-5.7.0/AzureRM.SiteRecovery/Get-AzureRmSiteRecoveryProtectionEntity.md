---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 851978fafa35d36923adf4dd2c2a6e071c054d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679692"
---
# <span data-ttu-id="f19a1-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f19a1-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="f19a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f19a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f19a1-103">Beolvassa a védett vagy a védett entitások listáját az aktuális webhely-helyreállítási boltozattal.</span><span class="sxs-lookup"><span data-stu-id="f19a1-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f19a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f19a1-104">SYNTAX</span></span>

### <span data-ttu-id="f19a1-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f19a1-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f19a1-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f19a1-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f19a1-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f19a1-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f19a1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f19a1-108">DESCRIPTION</span></span>
<span data-ttu-id="f19a1-109">A **Get-AzureRmSiteRecoveryProtectionEntity** parancsmag a védett vagy a védett entitások (például virtuális gépek) listáját a jelenlegi Azure webhely-helyreállítási boltozatban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f19a1-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f19a1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f19a1-110">EXAMPLES</span></span>

## <span data-ttu-id="f19a1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f19a1-111">PARAMETERS</span></span>

### <span data-ttu-id="f19a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19a1-112">-DefaultProfile</span></span>
<span data-ttu-id="f19a1-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f19a1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f19a1-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="f19a1-114">-FriendlyName</span></span>
<span data-ttu-id="f19a1-115">A védelmi entitás rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f19a1-115">Specifies the friendly name of the protection entity.</span></span>

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

### <span data-ttu-id="f19a1-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f19a1-116">-Name</span></span>
<span data-ttu-id="f19a1-117">A védelmi entitás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f19a1-117">Specifies the name of the protection entity.</span></span>

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

### <span data-ttu-id="f19a1-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f19a1-118">-ProtectionContainer</span></span>
<span data-ttu-id="f19a1-119">A Protection Container objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f19a1-119">Specifies the protection container object.</span></span>

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

### <span data-ttu-id="f19a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19a1-120">CommonParameters</span></span>
<span data-ttu-id="f19a1-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f19a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19a1-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f19a1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19a1-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f19a1-123">INPUTS</span></span>

### <span data-ttu-id="f19a1-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f19a1-124">ASRProtectionContainer</span></span>
<span data-ttu-id="f19a1-125">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f19a1-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="f19a1-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f19a1-126">OUTPUTS</span></span>

### <span data-ttu-id="f19a1-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="f19a1-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="f19a1-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f19a1-128">NOTES</span></span>

## <span data-ttu-id="f19a1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f19a1-129">RELATED LINKS</span></span>

[<span data-ttu-id="f19a1-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f19a1-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
