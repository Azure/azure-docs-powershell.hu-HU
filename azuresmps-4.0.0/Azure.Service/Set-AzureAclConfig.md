---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016432"
---
# <span data-ttu-id="6e092-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6e092-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="6e092-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e092-102">SYNOPSIS</span></span>
<span data-ttu-id="6e092-103">ACL-konfiguráció objektumának módosítása.</span><span class="sxs-lookup"><span data-stu-id="6e092-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="6e092-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e092-104">SYNTAX</span></span>

### <span data-ttu-id="6e092-105">AddRule</span><span class="sxs-lookup"><span data-stu-id="6e092-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6e092-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="6e092-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6e092-107">SetRule</span><span class="sxs-lookup"><span data-stu-id="6e092-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6e092-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e092-108">DESCRIPTION</span></span>
<span data-ttu-id="6e092-109">A **set-AzureAclConfig** parancsmag a hozzáférés-vezérlési listák (ACL) konfigurációs objektumait egy meglévő Azure Virtual Machine-konfigurációban módosítja.</span><span class="sxs-lookup"><span data-stu-id="6e092-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="6e092-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6e092-110">EXAMPLES</span></span>

### <span data-ttu-id="6e092-111">1. példa: szabály felvétele új ACL-konfigurációba</span><span class="sxs-lookup"><span data-stu-id="6e092-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="6e092-112">Az első parancs ACL-konfigurációt hoz létre, majd a $Acl változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6e092-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="6e092-113">A második parancs új szabályt ad hozzá a $Aclban tárolt konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="6e092-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="6e092-114">A parancs a szabály műveletét, alhálózatát, sorrendjét és leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e092-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="6e092-115">2. példa: szabály módosítása ACL-konfigurációban</span><span class="sxs-lookup"><span data-stu-id="6e092-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="6e092-116">Az első parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="6e092-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="6e092-117">A parancs átadja az objektumot a **Get-AzureAclConfig** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="6e092-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6e092-118">Ez a parancsmag a Web nevű végpont ACL-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6e092-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="6e092-119">A parancs az ACL konfigurációs objektumát az $Acl változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6e092-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="6e092-120">A második parancs módosítja a 0 AZONOSÍTÓJÚ szabályt.</span><span class="sxs-lookup"><span data-stu-id="6e092-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="6e092-121">A parancs módosítja a szabály sorrendjét és leírását.</span><span class="sxs-lookup"><span data-stu-id="6e092-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="6e092-122">A végleges parancs a **set-AzureEndpoint** parancsmaggal beállítja a virtuális gép ACL-konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="6e092-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="6e092-123">A parancs a virtuális gépet is frissíti.</span><span class="sxs-lookup"><span data-stu-id="6e092-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="6e092-124">3. példa: szabály eltávolítása ACL-konfigurációból</span><span class="sxs-lookup"><span data-stu-id="6e092-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="6e092-125">Az első parancs egy ACL-konfigurációs objektumot tárol a $Acl változóban.</span><span class="sxs-lookup"><span data-stu-id="6e092-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="6e092-126">Ugyanaz, mint az előző példában.</span><span class="sxs-lookup"><span data-stu-id="6e092-126">This is the same as the previous example.</span></span>

<span data-ttu-id="6e092-127">A második parancs eltávolítja a 0 AZONOSÍTÓJÚ szabályt az $Acl ACL-konfigurációjától.</span><span class="sxs-lookup"><span data-stu-id="6e092-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="6e092-128">A végleges parancs beállítja a virtuális gép ACL-konfigurációs objektumát, és frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="6e092-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="6e092-129">Ugyanaz, mint az előző példában.</span><span class="sxs-lookup"><span data-stu-id="6e092-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="6e092-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e092-130">PARAMETERS</span></span>

### <span data-ttu-id="6e092-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="6e092-131">-ACL</span></span>
<span data-ttu-id="6e092-132">Olyan ACL-konfigurációs objektumot ad meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="6e092-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-133">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="6e092-133">-Action</span></span>
<span data-ttu-id="6e092-134">A parancsmag által hozzáadott vagy módosított szabályra vonatkozó műveleteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e092-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="6e092-135">Az érvényes értékek a következők: engedélyezés és megtagadás.</span><span class="sxs-lookup"><span data-stu-id="6e092-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-136">-AddRule</span><span class="sxs-lookup"><span data-stu-id="6e092-136">-AddRule</span></span>
<span data-ttu-id="6e092-137">Jelzi, hogy ez a parancsmag szabályt ad az ACL-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="6e092-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-138">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6e092-138">-Description</span></span>
<span data-ttu-id="6e092-139">A parancsmag által hozzáadott vagy módosított szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e092-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6e092-140">-InformationAction</span></span>
<span data-ttu-id="6e092-141">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="6e092-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6e092-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6e092-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e092-143">Folytassa</span><span class="sxs-lookup"><span data-stu-id="6e092-143">Continue</span></span>
- <span data-ttu-id="6e092-144">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="6e092-144">Ignore</span></span>
- <span data-ttu-id="6e092-145">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="6e092-145">Inquire</span></span>
- <span data-ttu-id="6e092-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6e092-146">SilentlyContinue</span></span>
- <span data-ttu-id="6e092-147">állj</span><span class="sxs-lookup"><span data-stu-id="6e092-147">Stop</span></span>
- <span data-ttu-id="6e092-148">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="6e092-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6e092-149">-InformationVariable</span></span>
<span data-ttu-id="6e092-150">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="6e092-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-151">-Order (rendelés)</span><span class="sxs-lookup"><span data-stu-id="6e092-151">-Order</span></span>
<span data-ttu-id="6e092-152">A parancsmag által hozzáadott vagy módosított szabály feldolgozási sorrendjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e092-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="6e092-153">-RemoteSubnet</span></span>
<span data-ttu-id="6e092-154">A parancsmag által hozzáadott vagy módosított szabály távoli alhálózatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e092-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="6e092-155">Egy, az osztály nélküli tartományok közötti útválasztási (CIDR) formátumú címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e092-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="6e092-156">-RemoveRule</span></span>
<span data-ttu-id="6e092-157">Jelzi, hogy ez a parancsmag eltávolítja a szabályt az ACL-konfigurációból.</span><span class="sxs-lookup"><span data-stu-id="6e092-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-158">-RuleId</span><span class="sxs-lookup"><span data-stu-id="6e092-158">-RuleId</span></span>
<span data-ttu-id="6e092-159">Annak a szabálynak az AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja vagy módosította az ACL-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="6e092-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-160">-SetRule</span><span class="sxs-lookup"><span data-stu-id="6e092-160">-SetRule</span></span>
<span data-ttu-id="6e092-161">Jelzi, hogy az adott parancsmag módosította az ACL-konfiguráció szabályait.</span><span class="sxs-lookup"><span data-stu-id="6e092-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e092-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e092-162">CommonParameters</span></span>
<span data-ttu-id="6e092-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e092-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e092-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e092-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e092-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e092-165">INPUTS</span></span>

## <span data-ttu-id="6e092-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e092-166">OUTPUTS</span></span>

## <span data-ttu-id="6e092-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e092-167">NOTES</span></span>

## <span data-ttu-id="6e092-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e092-168">RELATED LINKS</span></span>

[<span data-ttu-id="6e092-169">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6e092-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="6e092-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6e092-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="6e092-171">Új – AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6e092-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="6e092-172">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6e092-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="6e092-173">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e092-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="6e092-174">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6e092-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


