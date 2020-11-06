---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 0ef59a8071438fa1bfd1560ab2f2102722aa335f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494669"
---
# <span data-ttu-id="600c1-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="600c1-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="600c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="600c1-102">SYNOPSIS</span></span>
<span data-ttu-id="600c1-103">A fürt biztonságához használt fürtcsomópontok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="600c1-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="600c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="600c1-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="600c1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="600c1-105">DESCRIPTION</span></span>
<span data-ttu-id="600c1-106">**Távolítsa** el a AzureRmServiceFabricClusterCertificate a fürtből, amíg a fürtben már használatban van egy másik érvényes tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="600c1-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="600c1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="600c1-107">EXAMPLES</span></span>

### <span data-ttu-id="600c1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="600c1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="600c1-109">Ez a parancs eltávolítja a tanúsítványt, amelyben az ujjlenyomat-5F3660C715EBBDA31DB1FFDCF508302348DE8E7A a fürtök biztonsága szempontjából használatban van.</span><span class="sxs-lookup"><span data-stu-id="600c1-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="600c1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="600c1-110">PARAMETERS</span></span>

### <span data-ttu-id="600c1-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="600c1-111">-Name</span></span>
<span data-ttu-id="600c1-112">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="600c1-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600c1-113">-ResourceGroupName</span></span>
<span data-ttu-id="600c1-114">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="600c1-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c1-115">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="600c1-115">-Thumbprint</span></span>
<span data-ttu-id="600c1-116">Adja meg az eltávolítandó szektorcsoport-ujjlenyomatot.</span><span class="sxs-lookup"><span data-stu-id="600c1-116">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="600c1-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="600c1-117">-Confirm</span></span>
<span data-ttu-id="600c1-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="600c1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600c1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600c1-119">-WhatIf</span></span>
<span data-ttu-id="600c1-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="600c1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="600c1-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="600c1-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600c1-122">-DefaultProfile</span></span>
<span data-ttu-id="600c1-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="600c1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="600c1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600c1-124">CommonParameters</span></span>
<span data-ttu-id="600c1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="600c1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600c1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="600c1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600c1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="600c1-127">INPUTS</span></span>

### <span data-ttu-id="600c1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="600c1-128">System.String</span></span>

## <span data-ttu-id="600c1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="600c1-129">OUTPUTS</span></span>

### <span data-ttu-id="600c1-130">Microsoft. Azure. Command. ServiceFabric. models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="600c1-130">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="600c1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="600c1-131">NOTES</span></span>

## <span data-ttu-id="600c1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="600c1-132">RELATED LINKS</span></span>

