---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672685"
---
# <span data-ttu-id="dc521-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="dc521-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="dc521-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc521-102">SYNOPSIS</span></span>
<span data-ttu-id="dc521-103">Információt kap a webhely-helyreállítási felügyelt virtuális gépekről.</span><span class="sxs-lookup"><span data-stu-id="dc521-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc521-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc521-104">SYNTAX</span></span>

### <span data-ttu-id="dc521-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc521-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc521-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="dc521-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc521-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="dc521-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc521-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc521-108">DESCRIPTION</span></span>
<span data-ttu-id="dc521-109">A **Get-AzureRmSiteRecoveryVM** parancsmag információt kap az Azure webhely-helyreállítással kezelt virtuális gépekről.</span><span class="sxs-lookup"><span data-stu-id="dc521-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="dc521-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dc521-110">EXAMPLES</span></span>

## <span data-ttu-id="dc521-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc521-111">PARAMETERS</span></span>

### <span data-ttu-id="dc521-112">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="dc521-112">-FriendlyName</span></span>
<span data-ttu-id="dc521-113">A virtuális gép rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc521-113">Specifies the friendly name of the virtual machine.</span></span>

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

### <span data-ttu-id="dc521-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc521-114">-Name</span></span>
<span data-ttu-id="dc521-115">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc521-115">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="dc521-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dc521-116">-ProtectionContainer</span></span>
<span data-ttu-id="dc521-117">A webhely-helyreállítási védelem tárolójának objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc521-117">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc521-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc521-118">-DefaultProfile</span></span>
<span data-ttu-id="dc521-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc521-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc521-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc521-120">CommonParameters</span></span>
<span data-ttu-id="dc521-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc521-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc521-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc521-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc521-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc521-123">INPUTS</span></span>

### <span data-ttu-id="dc521-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dc521-124">ASRProtectionContainer</span></span>
<span data-ttu-id="dc521-125">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dc521-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="dc521-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dc521-126">ASRProtectionContainer</span></span>
<span data-ttu-id="dc521-127">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dc521-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="dc521-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc521-128">OUTPUTS</span></span>

### <span data-ttu-id="dc521-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="dc521-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="dc521-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc521-130">NOTES</span></span>

## <span data-ttu-id="dc521-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc521-131">RELATED LINKS</span></span>

[<span data-ttu-id="dc521-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="dc521-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
