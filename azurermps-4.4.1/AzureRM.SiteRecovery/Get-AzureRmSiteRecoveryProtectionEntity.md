---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504724"
---
# <span data-ttu-id="222ac-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="222ac-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="222ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="222ac-102">SYNOPSIS</span></span>
<span data-ttu-id="222ac-103">Beolvassa a védett vagy a védett entitások listáját az aktuális webhely-helyreállítási boltozattal.</span><span class="sxs-lookup"><span data-stu-id="222ac-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="222ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="222ac-104">SYNTAX</span></span>

### <span data-ttu-id="222ac-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="222ac-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="222ac-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="222ac-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="222ac-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="222ac-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="222ac-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="222ac-108">DESCRIPTION</span></span>
<span data-ttu-id="222ac-109">A **Get-AzureRmSiteRecoveryProtectionEntity** parancsmag a védett vagy a védett entitások (például virtuális gépek) listáját a jelenlegi Azure webhely-helyreállítási boltozatban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="222ac-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="222ac-110">Példák</span><span class="sxs-lookup"><span data-stu-id="222ac-110">EXAMPLES</span></span>

## <span data-ttu-id="222ac-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="222ac-111">PARAMETERS</span></span>

### <span data-ttu-id="222ac-112">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="222ac-112">-FriendlyName</span></span>
<span data-ttu-id="222ac-113">A védelmi entitás rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="222ac-113">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222ac-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="222ac-114">-Name</span></span>
<span data-ttu-id="222ac-115">A védelmi entitás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="222ac-115">Specifies the name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222ac-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="222ac-116">-ProtectionContainer</span></span>
<span data-ttu-id="222ac-117">A Protection Container objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="222ac-117">Specifies the protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="222ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222ac-118">-DefaultProfile</span></span>
<span data-ttu-id="222ac-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="222ac-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="222ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="222ac-120">CommonParameters</span></span>
<span data-ttu-id="222ac-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="222ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="222ac-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="222ac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="222ac-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="222ac-123">INPUTS</span></span>

### <span data-ttu-id="222ac-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="222ac-124">ASRProtectionContainer</span></span>
<span data-ttu-id="222ac-125">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="222ac-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="222ac-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="222ac-126">OUTPUTS</span></span>

### <span data-ttu-id="222ac-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="222ac-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="222ac-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="222ac-128">NOTES</span></span>

## <span data-ttu-id="222ac-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="222ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="222ac-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="222ac-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
