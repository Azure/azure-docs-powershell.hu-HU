---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465888"
---
# <span data-ttu-id="832fa-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="832fa-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="832fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="832fa-102">SYNOPSIS</span></span>
<span data-ttu-id="832fa-103">IP-címke objektumot hoz létre a VMSS hálózati felületére.</span><span class="sxs-lookup"><span data-stu-id="832fa-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="832fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="832fa-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="832fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="832fa-105">DESCRIPTION</span></span>
<span data-ttu-id="832fa-106">A **New-AzVmssIpTagConfig** parancsmag IP-címkekonfigurációs objektumot hoz létre egy virtuálisgép-mérethalmaz (VMSS) hálózati felületének.</span><span class="sxs-lookup"><span data-stu-id="832fa-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="832fa-107">Adja meg a parancsmag konfigurációját a New-AzVmssIpConfig *IPTag* paramétereként.</span><span class="sxs-lookup"><span data-stu-id="832fa-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="832fa-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="832fa-108">EXAMPLES</span></span>

### <span data-ttu-id="832fa-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="832fa-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="832fa-110">Ez a parancs létrehoz egy IP-címke helyi objektumot "FirstPartyUsage" típusú és "Sql" címkével, majd létrehoz egy IP-konfigurációt ezzel az IP-címkével.</span><span class="sxs-lookup"><span data-stu-id="832fa-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="832fa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="832fa-111">PARAMETERS</span></span>

### <span data-ttu-id="832fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="832fa-112">-DefaultProfile</span></span>
<span data-ttu-id="832fa-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="832fa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="832fa-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="832fa-114">-IpTagType</span></span>
<span data-ttu-id="832fa-115">IP-címketípust ad meg.</span><span class="sxs-lookup"><span data-stu-id="832fa-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="832fa-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="832fa-116">-Tag</span></span>
<span data-ttu-id="832fa-117">IP-címkeértéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="832fa-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="832fa-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="832fa-118">-Confirm</span></span>
<span data-ttu-id="832fa-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="832fa-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="832fa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="832fa-120">-WhatIf</span></span>
<span data-ttu-id="832fa-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="832fa-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="832fa-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="832fa-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="832fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="832fa-123">CommonParameters</span></span>
<span data-ttu-id="832fa-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="832fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="832fa-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="832fa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="832fa-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="832fa-126">INPUTS</span></span>

### <span data-ttu-id="832fa-127">System.String</span><span class="sxs-lookup"><span data-stu-id="832fa-127">System.String</span></span>

## <span data-ttu-id="832fa-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="832fa-128">OUTPUTS</span></span>

### <span data-ttu-id="832fa-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="832fa-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="832fa-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="832fa-130">NOTES</span></span>

## <span data-ttu-id="832fa-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="832fa-131">RELATED LINKS</span></span>
