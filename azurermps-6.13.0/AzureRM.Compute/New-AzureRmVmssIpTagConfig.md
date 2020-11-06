---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
ms.openlocfilehash: a77680921eeef0a678cbd83d04bef9a51cf35cb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491991"
---
# <span data-ttu-id="5065d-101">New-AzureRmVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="5065d-101">New-AzureRmVmssIpTagConfig</span></span>

## <span data-ttu-id="5065d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5065d-102">SYNOPSIS</span></span>
<span data-ttu-id="5065d-103">IP-címke típusú objektumot hoz létre egy VMSS hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="5065d-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5065d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5065d-104">SYNTAX</span></span>

```
New-AzureRmVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5065d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5065d-105">DESCRIPTION</span></span>
<span data-ttu-id="5065d-106">A **New-AzureRmVmssIpTagConfig** parancsmag létrehoz egy IP-címkés konfigurációs objektumot a virtuálisgép-készlet (VMSS) hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="5065d-106">The **New-AzureRmVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="5065d-107">Adja meg a parancsmag konfigurációját az New-AzureRmVmssIpConfig parancsmag *IPTag* paramétereként.</span><span class="sxs-lookup"><span data-stu-id="5065d-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzureRmVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="5065d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5065d-108">EXAMPLES</span></span>

### <span data-ttu-id="5065d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5065d-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzureRmVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzureRmVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="5065d-110">A parancs létrehozza az IP-címke helyi objektumát a "FirstPartyUsage" és az "SQL" címkével, majd létrehoz egy IP-konfigurációt ezzel az IP-kóddal.</span><span class="sxs-lookup"><span data-stu-id="5065d-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="5065d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5065d-111">PARAMETERS</span></span>

### <span data-ttu-id="5065d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5065d-112">-DefaultProfile</span></span>
<span data-ttu-id="5065d-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5065d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5065d-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="5065d-114">-IpTagType</span></span>
<span data-ttu-id="5065d-115">Az IP-címke típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5065d-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="5065d-116">-Címke</span><span class="sxs-lookup"><span data-stu-id="5065d-116">-Tag</span></span>
<span data-ttu-id="5065d-117">Az IP-címke értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5065d-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="5065d-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5065d-118">-Confirm</span></span>
<span data-ttu-id="5065d-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5065d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5065d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5065d-120">-WhatIf</span></span>
<span data-ttu-id="5065d-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5065d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5065d-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5065d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5065d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5065d-123">CommonParameters</span></span>
<span data-ttu-id="5065d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5065d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5065d-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5065d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5065d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5065d-126">INPUTS</span></span>

### <span data-ttu-id="5065d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5065d-127">System.String</span></span>

## <span data-ttu-id="5065d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5065d-128">OUTPUTS</span></span>

### <span data-ttu-id="5065d-129">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="5065d-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="5065d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5065d-130">NOTES</span></span>

## <span data-ttu-id="5065d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5065d-131">RELATED LINKS</span></span>
