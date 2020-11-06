---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 3d4530090bc1386a34056b315c79a826be5d771f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496839"
---
# <span data-ttu-id="b8401-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b8401-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="b8401-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8401-102">SYNOPSIS</span></span>
<span data-ttu-id="b8401-103">Az Azure webhely-helyreállítási anyag eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b8401-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8401-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8401-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8401-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8401-105">DESCRIPTION</span></span>
<span data-ttu-id="b8401-106">A **Remove-AzureRmSiteRecoveryFabric** parancsmag eltávolítja az Azure-webhelyek helyreállítási szövetét.</span><span class="sxs-lookup"><span data-stu-id="b8401-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="b8401-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b8401-107">EXAMPLES</span></span>

## <span data-ttu-id="b8401-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8401-108">PARAMETERS</span></span>

### <span data-ttu-id="b8401-109">-Szövet</span><span class="sxs-lookup"><span data-stu-id="b8401-109">-Fabric</span></span>
<span data-ttu-id="b8401-110">Az Azure site Recovery Fabric objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8401-110">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8401-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b8401-111">-Force</span></span>
<span data-ttu-id="b8401-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b8401-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8401-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8401-113">-Confirm</span></span>
<span data-ttu-id="b8401-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8401-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8401-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8401-115">-WhatIf</span></span>
<span data-ttu-id="b8401-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8401-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b8401-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8401-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8401-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8401-118">-DefaultProfile</span></span>
<span data-ttu-id="b8401-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8401-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8401-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8401-120">CommonParameters</span></span>
<span data-ttu-id="b8401-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8401-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8401-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8401-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8401-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8401-123">INPUTS</span></span>

### <span data-ttu-id="b8401-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b8401-124">ASRFabric</span></span>
<span data-ttu-id="b8401-125">A "szövet" paraméter az "ASRFabric" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b8401-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="b8401-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8401-126">OUTPUTS</span></span>

### <span data-ttu-id="b8401-127">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b8401-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b8401-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8401-128">NOTES</span></span>

## <span data-ttu-id="b8401-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8401-129">RELATED LINKS</span></span>

[<span data-ttu-id="b8401-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b8401-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="b8401-131">Új – AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b8401-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
