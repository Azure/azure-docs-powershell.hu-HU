---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 1cdcbad6af048d7fc462dbe8a28fdd02fd576aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502388"
---
# <span data-ttu-id="4c9ee-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="4c9ee-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="4c9ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9ee-103">Információt kap a webhely-helyreállítási felügyelt virtuális gépekről.</span><span class="sxs-lookup"><span data-stu-id="4c9ee-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c9ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c9ee-104">SYNTAX</span></span>

### <span data-ttu-id="4c9ee-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c9ee-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9ee-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4c9ee-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9ee-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4c9ee-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c9ee-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c9ee-108">DESCRIPTION</span></span>
<span data-ttu-id="4c9ee-109">A **Get-AzureRmSiteRecoveryVM** parancsmag információt kap az Azure webhely-helyreállítással kezelt virtuális gépekről.</span><span class="sxs-lookup"><span data-stu-id="4c9ee-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="4c9ee-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4c9ee-110">EXAMPLES</span></span>

## <span data-ttu-id="4c9ee-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c9ee-111">PARAMETERS</span></span>

### <span data-ttu-id="4c9ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9ee-112">-DefaultProfile</span></span>
<span data-ttu-id="4c9ee-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c9ee-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c9ee-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="4c9ee-114">-FriendlyName</span></span>
<span data-ttu-id="4c9ee-115">A virtuális gép rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ee-115">Specifies the friendly name of the virtual machine.</span></span>

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

### <span data-ttu-id="4c9ee-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c9ee-116">-Name</span></span>
<span data-ttu-id="4c9ee-117">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ee-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="4c9ee-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4c9ee-118">-ProtectionContainer</span></span>
<span data-ttu-id="4c9ee-119">A webhely-helyreállítási védelem tárolójának objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ee-119">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9ee-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9ee-120">CommonParameters</span></span>
<span data-ttu-id="4c9ee-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c9ee-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9ee-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c9ee-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9ee-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c9ee-123">INPUTS</span></span>

### <span data-ttu-id="4c9ee-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4c9ee-124">ASRProtectionContainer</span></span>
<span data-ttu-id="4c9ee-125">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4c9ee-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="4c9ee-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4c9ee-126">ASRProtectionContainer</span></span>
<span data-ttu-id="4c9ee-127">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4c9ee-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="4c9ee-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c9ee-128">OUTPUTS</span></span>

### <span data-ttu-id="4c9ee-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="4c9ee-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="4c9ee-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c9ee-130">NOTES</span></span>

## <span data-ttu-id="4c9ee-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c9ee-131">RELATED LINKS</span></span>

[<span data-ttu-id="4c9ee-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="4c9ee-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
