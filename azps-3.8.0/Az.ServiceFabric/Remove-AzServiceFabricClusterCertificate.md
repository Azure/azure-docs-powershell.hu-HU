---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 3d5f3ce0e941d8359087db792cdf3c8a721bba39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011710"
---
# <span data-ttu-id="38cd0-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="38cd0-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="38cd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="38cd0-103">A fürt biztonságához használt fürtcsomópontok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="38cd0-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="38cd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38cd0-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38cd0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="38cd0-106">**Távolítsa** el a AzServiceFabricClusterCertificate a fürtből, amíg a fürtben már használatban van egy másik érvényes tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="38cd0-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="38cd0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="38cd0-107">EXAMPLES</span></span>

### <span data-ttu-id="38cd0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="38cd0-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="38cd0-109">Ez a parancs eltávolítja a tanúsítványt, amelyben az ujjlenyomat-5F3660C715EBBDA31DB1FFDCF508302348DE8E7A a fürtök biztonsága szempontjából használatban van.</span><span class="sxs-lookup"><span data-stu-id="38cd0-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="38cd0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38cd0-110">PARAMETERS</span></span>

### <span data-ttu-id="38cd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38cd0-111">-DefaultProfile</span></span>
<span data-ttu-id="38cd0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38cd0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38cd0-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38cd0-113">-Name</span></span>
<span data-ttu-id="38cd0-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="38cd0-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="38cd0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38cd0-115">-ResourceGroupName</span></span>
<span data-ttu-id="38cd0-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38cd0-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="38cd0-117">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="38cd0-117">-Thumbprint</span></span>
<span data-ttu-id="38cd0-118">Adja meg az eltávolítandó szektorcsoport-ujjlenyomatot.</span><span class="sxs-lookup"><span data-stu-id="38cd0-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="38cd0-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38cd0-119">-Confirm</span></span>
<span data-ttu-id="38cd0-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38cd0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38cd0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38cd0-121">-WhatIf</span></span>
<span data-ttu-id="38cd0-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38cd0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38cd0-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38cd0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38cd0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38cd0-124">CommonParameters</span></span>
<span data-ttu-id="38cd0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38cd0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38cd0-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38cd0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38cd0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38cd0-127">INPUTS</span></span>

### <span data-ttu-id="38cd0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="38cd0-128">System.String</span></span>

## <span data-ttu-id="38cd0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38cd0-129">OUTPUTS</span></span>

### <span data-ttu-id="38cd0-130">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="38cd0-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="38cd0-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38cd0-131">NOTES</span></span>

## <span data-ttu-id="38cd0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38cd0-132">RELATED LINKS</span></span>
