---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: 241b8938be77d9074000a116f82d8b2bcdffc5b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007077"
---
# <span data-ttu-id="6263f-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="6263f-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="6263f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6263f-102">SYNOPSIS</span></span>
<span data-ttu-id="6263f-103">IP-címke objektumot hoz létre a VMSS hálózati felületére.</span><span class="sxs-lookup"><span data-stu-id="6263f-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="6263f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6263f-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6263f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6263f-105">DESCRIPTION</span></span>
<span data-ttu-id="6263f-106">A **New-AzVmssIpTagConfig** parancsmag IP-címkekonfigurációs objektumot hoz létre egy virtuálisgép-mérethalmaz (VMSS) hálózati felületének.</span><span class="sxs-lookup"><span data-stu-id="6263f-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="6263f-107">Adja meg a parancsmag konfigurációját a New-AzVmssIpConfig *IPTag* paramétereként.</span><span class="sxs-lookup"><span data-stu-id="6263f-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="6263f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6263f-108">EXAMPLES</span></span>

### <span data-ttu-id="6263f-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="6263f-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="6263f-110">Ez a parancs létrehoz egy IP-címke helyi objektumot "FirstPartyUsage" típusú és "Sql" címkével, majd létrehoz egy IP-konfigurációt ezzel az IP-címkével.</span><span class="sxs-lookup"><span data-stu-id="6263f-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="6263f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6263f-111">PARAMETERS</span></span>

### <span data-ttu-id="6263f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6263f-112">-DefaultProfile</span></span>
<span data-ttu-id="6263f-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6263f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6263f-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="6263f-114">-IpTagType</span></span>
<span data-ttu-id="6263f-115">IP-címketípust ad meg.</span><span class="sxs-lookup"><span data-stu-id="6263f-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="6263f-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="6263f-116">-Tag</span></span>
<span data-ttu-id="6263f-117">IP-címkeértéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="6263f-117">Specifies an IP Tag Value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6263f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6263f-118">-Confirm</span></span>
<span data-ttu-id="6263f-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6263f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6263f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6263f-120">-WhatIf</span></span>
<span data-ttu-id="6263f-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6263f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6263f-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6263f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6263f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6263f-123">CommonParameters</span></span>
<span data-ttu-id="6263f-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6263f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6263f-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6263f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6263f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6263f-126">INPUTS</span></span>

### <span data-ttu-id="6263f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6263f-127">System.String</span></span>

## <span data-ttu-id="6263f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6263f-128">OUTPUTS</span></span>

### <span data-ttu-id="6263f-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="6263f-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="6263f-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6263f-130">NOTES</span></span>

## <span data-ttu-id="6263f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6263f-131">RELATED LINKS</span></span>
