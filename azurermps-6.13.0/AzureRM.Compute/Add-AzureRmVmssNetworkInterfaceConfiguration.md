---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 6789b2a0f3309e8011cc6e87a27dbf9f28579d05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496343"
---
# <span data-ttu-id="6b326-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b326-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="6b326-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b326-102">SYNOPSIS</span></span>
<span data-ttu-id="6b326-103">Hálózati illesztőfelület-konfiguráció felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b326-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b326-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b326-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b326-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b326-105">DESCRIPTION</span></span>
<span data-ttu-id="6b326-106">Az **Add-AzureRmVmssNetworkInterfaceConfiguration** parancsmag hálózati illesztőfelület-konfigurációt ad hozzá a Virtual Machine Scale set (VMSS) beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="6b326-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="6b326-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6b326-107">EXAMPLES</span></span>

### <span data-ttu-id="6b326-108">Példa 1: hálózati illesztőfelület-konfiguráció felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="6b326-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="6b326-109">Ez a parancs hálózati illesztőfelület-konfigurációt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b326-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="6b326-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b326-110">PARAMETERS</span></span>

### <span data-ttu-id="6b326-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b326-111">-DefaultProfile</span></span>
<span data-ttu-id="6b326-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b326-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b326-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="6b326-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="6b326-114">A DNS-kiszolgálók IP-címeinek listája a DNS-beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="6b326-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="6b326-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="6b326-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="6b326-116">Azt adja meg, hogy a hálózati felület gyorsított hálózati kapcsolaton van-e.</span><span class="sxs-lookup"><span data-stu-id="6b326-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="6b326-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="6b326-117">-EnableIPForwarding</span></span>
<span data-ttu-id="6b326-118">Megadja, hogy engedélyezve van-e az IP-továbbítás ezen a NIC-ben.</span><span class="sxs-lookup"><span data-stu-id="6b326-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="6b326-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="6b326-119">-Id</span></span>
<span data-ttu-id="6b326-120">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b326-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="6b326-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b326-121">-IpConfiguration</span></span>
<span data-ttu-id="6b326-122">A hálózati felület IP-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b326-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="6b326-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b326-123">-Name</span></span>
<span data-ttu-id="6b326-124">A hálózati felület konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b326-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="6b326-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6b326-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="6b326-126">A hálózati biztonsági csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="6b326-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="6b326-127">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="6b326-127">-Primary</span></span>
<span data-ttu-id="6b326-128">Azt jelzi, hogy a hálózati illesztőfelület-konfigurációból létrehozott hálózati felületek a virtuális gép elsődleges hálózati információs központja (NIC) fogják-e létrehozni.</span><span class="sxs-lookup"><span data-stu-id="6b326-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="6b326-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b326-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6b326-130">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b326-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="6b326-131">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6b326-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="6b326-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6b326-132">-Confirm</span></span>
<span data-ttu-id="6b326-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b326-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b326-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b326-134">-WhatIf</span></span>
<span data-ttu-id="6b326-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6b326-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b326-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b326-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b326-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b326-137">CommonParameters</span></span>
<span data-ttu-id="6b326-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b326-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b326-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b326-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b326-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b326-140">INPUTS</span></span>

### <span data-ttu-id="6b326-141">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b326-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6b326-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6b326-142">System.String</span></span>

### <span data-ttu-id="6b326-143">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6b326-143">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6b326-144">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6b326-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="6b326-145">System. string []</span><span class="sxs-lookup"><span data-stu-id="6b326-145">System.String[]</span></span>

## <span data-ttu-id="6b326-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b326-146">OUTPUTS</span></span>

### <span data-ttu-id="6b326-147">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b326-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6b326-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b326-148">NOTES</span></span>

## <span data-ttu-id="6b326-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b326-149">RELATED LINKS</span></span>

[<span data-ttu-id="6b326-150">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6b326-150">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
