---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 9e52131bd5f53d48b4c958c26a0ef37b5ebd23ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370760"
---
# <span data-ttu-id="bc0db-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc0db-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="bc0db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc0db-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0db-103">Hálózati felületi konfigurációt ad a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="bc0db-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="bc0db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bc0db-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc0db-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bc0db-105">DESCRIPTION</span></span>
<span data-ttu-id="bc0db-106">Az **Add-AzVmssNetworkInterfaceConfiguration** parancsmag hozzáad egy hálózati felületi konfigurációt a virtuális gép mérethalmazához (VMSS).</span><span class="sxs-lookup"><span data-stu-id="bc0db-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="bc0db-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bc0db-107">EXAMPLES</span></span>

### <span data-ttu-id="bc0db-108">1. példa: Hálózati felület konfigurációjának hozzáadása a VMSS-hez</span><span class="sxs-lookup"><span data-stu-id="bc0db-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="bc0db-109">Ez a parancs hozzáad egy hálózati felületi konfigurációt a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="bc0db-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="bc0db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc0db-110">PARAMETERS</span></span>

### <span data-ttu-id="bc0db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0db-111">-DefaultProfile</span></span>
<span data-ttu-id="bc0db-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc0db-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc0db-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="bc0db-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="bc0db-114">A DNS-beállítások DNS-kiszolgálói IP-címeinek listája.</span><span class="sxs-lookup"><span data-stu-id="bc0db-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0db-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="bc0db-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="bc0db-116">Meghatározza, hogy a hálózati felület gyorsítsa-e a hálózatépítést.</span><span class="sxs-lookup"><span data-stu-id="bc0db-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="bc0db-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="bc0db-117">-EnableIPForwarding</span></span>
<span data-ttu-id="bc0db-118">Azt adja meg, hogy engedélyezve van-e az IP-továbbítás ezen a NIC-on.</span><span class="sxs-lookup"><span data-stu-id="bc0db-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="bc0db-119">-Id</span><span class="sxs-lookup"><span data-stu-id="bc0db-119">-Id</span></span>
<span data-ttu-id="bc0db-120">A virtuális gép erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc0db-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0db-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc0db-121">-IpConfiguration</span></span>
<span data-ttu-id="bc0db-122">A hálózati felület IP-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc0db-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0db-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bc0db-123">-Name</span></span>
<span data-ttu-id="bc0db-124">A hálózati felület konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc0db-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0db-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bc0db-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="bc0db-126">A hálózati biztonsági csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bc0db-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="bc0db-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="bc0db-127">-Primary</span></span>
<span data-ttu-id="bc0db-128">Azt jelzi, hogy a hálózati felület konfigurációja alapján létrehozott hálózati felületek lesznek-e a virtuális gép elsődleges hálózati információs központja (NIC).</span><span class="sxs-lookup"><span data-stu-id="bc0db-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0db-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc0db-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bc0db-130">A VMSS-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc0db-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="bc0db-131">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bc0db-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0db-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc0db-132">-Confirm</span></span>
<span data-ttu-id="bc0db-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bc0db-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc0db-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc0db-134">-WhatIf</span></span>
<span data-ttu-id="bc0db-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bc0db-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc0db-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc0db-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc0db-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0db-137">CommonParameters</span></span>
<span data-ttu-id="bc0db-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc0db-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0db-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc0db-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0db-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc0db-140">INPUTS</span></span>

### <span data-ttu-id="bc0db-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc0db-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="bc0db-142">System.String</span><span class="sxs-lookup"><span data-stu-id="bc0db-142">System.String</span></span>

### <span data-ttu-id="bc0db-143">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc0db-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bc0db-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="bc0db-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="bc0db-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bc0db-145">System.String[]</span></span>

## <span data-ttu-id="bc0db-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc0db-146">OUTPUTS</span></span>

### <span data-ttu-id="bc0db-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc0db-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bc0db-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bc0db-148">NOTES</span></span>

## <span data-ttu-id="bc0db-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc0db-149">RELATED LINKS</span></span>

[<span data-ttu-id="bc0db-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bc0db-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
