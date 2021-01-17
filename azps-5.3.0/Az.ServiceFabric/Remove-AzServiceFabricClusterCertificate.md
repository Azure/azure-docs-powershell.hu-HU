---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479542"
---
# <span data-ttu-id="07ba3-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="07ba3-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="07ba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="07ba3-103">Távolítsa el a fürt tanúsítványát a fürtbiztonság érdekében.</span><span class="sxs-lookup"><span data-stu-id="07ba3-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="07ba3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07ba3-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07ba3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07ba3-105">DESCRIPTION</span></span>
<span data-ttu-id="07ba3-106">A **Remove-AzServiceFabricClusterCertificate** segítségével eltávolíthat egy fürttanúsítványt a fürtből, ha van egy másik érvényes tanúsítvány, amely már használatban van a fürtben.</span><span class="sxs-lookup"><span data-stu-id="07ba3-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="07ba3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07ba3-107">EXAMPLES</span></span>

### <span data-ttu-id="07ba3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="07ba3-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="07ba3-109">Ez a parancs eltávolítja az 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A tanúsítványt a fürtbiztonság érdekében.</span><span class="sxs-lookup"><span data-stu-id="07ba3-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="07ba3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07ba3-110">PARAMETERS</span></span>

### <span data-ttu-id="07ba3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ba3-111">-DefaultProfile</span></span>
<span data-ttu-id="07ba3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07ba3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07ba3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="07ba3-113">-Name</span></span>
<span data-ttu-id="07ba3-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="07ba3-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="07ba3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ba3-115">-ResourceGroupName</span></span>
<span data-ttu-id="07ba3-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07ba3-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="07ba3-117">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="07ba3-117">-Thumbprint</span></span>
<span data-ttu-id="07ba3-118">Adja meg az eltávolítani kívánt fürt thumbprint.</span><span class="sxs-lookup"><span data-stu-id="07ba3-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="07ba3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07ba3-119">-Confirm</span></span>
<span data-ttu-id="07ba3-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="07ba3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07ba3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ba3-121">-WhatIf</span></span>
<span data-ttu-id="07ba3-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="07ba3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07ba3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07ba3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07ba3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ba3-124">CommonParameters</span></span>
<span data-ttu-id="07ba3-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ba3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ba3-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07ba3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ba3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07ba3-127">INPUTS</span></span>

### <span data-ttu-id="07ba3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="07ba3-128">System.String</span></span>

## <span data-ttu-id="07ba3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07ba3-129">OUTPUTS</span></span>

### <span data-ttu-id="07ba3-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="07ba3-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="07ba3-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07ba3-131">NOTES</span></span>

## <span data-ttu-id="07ba3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07ba3-132">RELATED LINKS</span></span>
