---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 03f898246b2f0d784725488f753697ed893b09df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015398"
---
# <span data-ttu-id="db66d-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="db66d-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="db66d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db66d-102">SYNOPSIS</span></span>
<span data-ttu-id="db66d-103">Hozzáad egy AD tartománybővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="db66d-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="db66d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db66d-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db66d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db66d-105">DESCRIPTION</span></span>
<span data-ttu-id="db66d-106">A **Set-AzVMADDomainExtension parancsmag** hozzáad egy Azure Active Directory (AD) tartomány virtuális gépbővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="db66d-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="db66d-107">Ez a bővítmény lehetővé teszi, hogy a virtuális gép csatlakozzon egy tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="db66d-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="db66d-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db66d-108">EXAMPLES</span></span>

## <span data-ttu-id="db66d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db66d-109">PARAMETERS</span></span>

### <span data-ttu-id="db66d-110">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="db66d-110">-Credential</span></span>
<span data-ttu-id="db66d-111">A virtuális gép felhasználónevét és jelszavát adja meg **PSCredential objektumként.**</span><span class="sxs-lookup"><span data-stu-id="db66d-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="db66d-112">Hitelesítő adatok beszerzéséhez használja a Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="db66d-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="db66d-113">További információért írja be a `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="db66d-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db66d-114">-DefaultProfile</span></span>
<span data-ttu-id="db66d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db66d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db66d-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="db66d-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="db66d-117">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziója automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="db66d-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="db66d-118">-DomainName</span></span>
<span data-ttu-id="db66d-119">A tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db66d-119">Specifies the name of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="db66d-120">-ForceRerun</span></span>
<span data-ttu-id="db66d-121">Azt jelzi, hogy ez a parancsmag a bővítmény eltávolítása és újratelepítése nélkül újrafuttatja ugyanazt a bővítménykonfigurációt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="db66d-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="db66d-122">Az érték bármilyen karakterlánc lehet, amely nem az aktuális érték.</span><span class="sxs-lookup"><span data-stu-id="db66d-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="db66d-123">Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit továbbra is alkalmazza a kezelő.</span><span class="sxs-lookup"><span data-stu-id="db66d-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="db66d-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="db66d-124">-JoinOption</span></span>
<span data-ttu-id="db66d-125">Az illesztés beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="db66d-125">Specifies the join option.</span></span> <span data-ttu-id="db66d-126">Az illesztési lehetőségekért [lásd: fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="db66d-126">For join options see [fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-127">-Location</span><span class="sxs-lookup"><span data-stu-id="db66d-127">-Location</span></span>
<span data-ttu-id="db66d-128">A virtuális gép helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="db66d-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="db66d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="db66d-129">-Name</span></span>
<span data-ttu-id="db66d-130">A hozzáadni megfelelő tartománybővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="db66d-130">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="db66d-131">-NoWait</span></span>
<span data-ttu-id="db66d-132">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="db66d-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="db66d-133">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="db66d-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="db66d-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="db66d-134">-OUPath</span></span>
<span data-ttu-id="db66d-135">A tartományfiók szervezeti egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db66d-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="db66d-136">Írja be a szervezeti egység teljes megkülönböztető nevét idézőjelek közé.</span><span class="sxs-lookup"><span data-stu-id="db66d-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="db66d-137">Az alapértelmezett érték a tartomány gépi objektumainál az alapértelmezett szervezeti egység.</span><span class="sxs-lookup"><span data-stu-id="db66d-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="db66d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db66d-138">-ResourceGroupName</span></span>
<span data-ttu-id="db66d-139">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db66d-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="db66d-140">-Újraindítás</span><span class="sxs-lookup"><span data-stu-id="db66d-140">-Restart</span></span>
<span data-ttu-id="db66d-141">Azt jelzi, hogy ez a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="db66d-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="db66d-142">A módosítás érvénybe hozása gyakran újraindítást igényel.</span><span class="sxs-lookup"><span data-stu-id="db66d-142">A restart is often required to make the change effective.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="db66d-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="db66d-144">A tartománybővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="db66d-144">Specifies the version of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="db66d-145">-VMName</span></span>
<span data-ttu-id="db66d-146">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db66d-146">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db66d-147">-Confirm</span></span>
<span data-ttu-id="db66d-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db66d-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db66d-149">-WhatIf</span></span>
<span data-ttu-id="db66d-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db66d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db66d-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db66d-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db66d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db66d-152">CommonParameters</span></span>
<span data-ttu-id="db66d-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db66d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db66d-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db66d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db66d-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db66d-155">INPUTS</span></span>

### <span data-ttu-id="db66d-156">System.String</span><span class="sxs-lookup"><span data-stu-id="db66d-156">System.String</span></span>

### <span data-ttu-id="db66d-157">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="db66d-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="db66d-158">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="db66d-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="db66d-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db66d-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db66d-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db66d-160">OUTPUTS</span></span>

### <span data-ttu-id="db66d-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="db66d-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="db66d-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db66d-162">NOTES</span></span>

## <span data-ttu-id="db66d-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db66d-163">RELATED LINKS</span></span>

[<span data-ttu-id="db66d-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="db66d-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
