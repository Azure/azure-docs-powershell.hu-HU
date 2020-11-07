---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: e29ee3c51b94964db286a999630196b46ad9f786
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837998"
---
# <span data-ttu-id="ac596-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ac596-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="ac596-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac596-102">SYNOPSIS</span></span>
<span data-ttu-id="ac596-103">A fürt biztonságához használt fürtcsomópontok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ac596-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="ac596-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac596-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac596-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac596-105">DESCRIPTION</span></span>
<span data-ttu-id="ac596-106">**Távolítsa** el a AzServiceFabricClusterCertificate a fürtből, amíg a fürtben már használatban van egy másik érvényes tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="ac596-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="ac596-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ac596-107">EXAMPLES</span></span>

### <span data-ttu-id="ac596-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac596-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="ac596-109">Ez a parancs eltávolítja a tanúsítványt, amelyben az ujjlenyomat-5F3660C715EBBDA31DB1FFDCF508302348DE8E7A a fürtök biztonsága szempontjából használatban van.</span><span class="sxs-lookup"><span data-stu-id="ac596-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="ac596-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac596-110">PARAMETERS</span></span>

### <span data-ttu-id="ac596-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac596-111">-DefaultProfile</span></span>
<span data-ttu-id="ac596-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac596-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac596-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac596-113">-Name</span></span>
<span data-ttu-id="ac596-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="ac596-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ac596-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac596-115">-ResourceGroupName</span></span>
<span data-ttu-id="ac596-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac596-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ac596-117">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="ac596-117">-Thumbprint</span></span>
<span data-ttu-id="ac596-118">Adja meg az eltávolítandó szektorcsoport-ujjlenyomatot.</span><span class="sxs-lookup"><span data-stu-id="ac596-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="ac596-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac596-119">-Confirm</span></span>
<span data-ttu-id="ac596-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac596-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac596-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac596-121">-WhatIf</span></span>
<span data-ttu-id="ac596-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac596-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac596-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac596-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac596-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac596-124">CommonParameters</span></span>
<span data-ttu-id="ac596-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac596-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac596-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac596-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac596-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac596-127">INPUTS</span></span>

### <span data-ttu-id="ac596-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ac596-128">System.String</span></span>

## <span data-ttu-id="ac596-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac596-129">OUTPUTS</span></span>

### <span data-ttu-id="ac596-130">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ac596-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ac596-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac596-131">NOTES</span></span>

## <span data-ttu-id="ac596-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac596-132">RELATED LINKS</span></span>
