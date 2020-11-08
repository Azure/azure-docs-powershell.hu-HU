---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 1ea90503c1d022aa5a1925fa489e2ee63f4560ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010917"
---
# <span data-ttu-id="5fa48-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5fa48-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="5fa48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fa48-102">SYNOPSIS</span></span>
<span data-ttu-id="5fa48-103">AD tartomány-kiterjesztést ad egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5fa48-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="5fa48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fa48-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fa48-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fa48-105">DESCRIPTION</span></span>
<span data-ttu-id="5fa48-106">A **set-AzVMADDomainExtension** parancsmag hozzáadja az Azure Active Directory (ad) domain Virtual Machine bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5fa48-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="5fa48-107">Ez a kiterjesztés lehetővé teszi, hogy a virtuális gép csatlakozzon a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="5fa48-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="5fa48-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5fa48-108">EXAMPLES</span></span>

## <span data-ttu-id="5fa48-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fa48-109">PARAMETERS</span></span>

### <span data-ttu-id="5fa48-110">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="5fa48-110">-Credential</span></span>
<span data-ttu-id="5fa48-111">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fa48-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="5fa48-112">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5fa48-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="5fa48-113">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="5fa48-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="5fa48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fa48-114">-DefaultProfile</span></span>
<span data-ttu-id="5fa48-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fa48-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fa48-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5fa48-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5fa48-117">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="5fa48-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="5fa48-118">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="5fa48-118">-DomainName</span></span>
<span data-ttu-id="5fa48-119">A tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fa48-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="5fa48-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5fa48-120">-ForceRerun</span></span>
<span data-ttu-id="5fa48-121">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5fa48-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5fa48-122">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="5fa48-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="5fa48-123">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="5fa48-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="5fa48-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="5fa48-124">-JoinOption</span></span>
<span data-ttu-id="5fa48-125">A csatlakozás lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fa48-125">Specifies the join option.</span></span> <span data-ttu-id="5fa48-126">Csatlakozás beállításai lásd: [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="5fa48-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="5fa48-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="5fa48-127">-Location</span></span>
<span data-ttu-id="5fa48-128">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fa48-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5fa48-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5fa48-129">-Name</span></span>
<span data-ttu-id="5fa48-130">Annak a tartománynak a nevét adja meg, amelybe fel szeretné venni a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="5fa48-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="5fa48-131">-Várva</span><span class="sxs-lookup"><span data-stu-id="5fa48-131">-NoWait</span></span>
<span data-ttu-id="5fa48-132">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="5fa48-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5fa48-133">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="5fa48-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5fa48-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="5fa48-134">-OUPath</span></span>
<span data-ttu-id="5fa48-135">A tartományi fiókhoz tartozó szervezeti egység (OU) meghatározása.</span><span class="sxs-lookup"><span data-stu-id="5fa48-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="5fa48-136">Adja meg a szervezeti egység teljes megkülönböztető nevét idézőjelek között.</span><span class="sxs-lookup"><span data-stu-id="5fa48-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="5fa48-137">Az alapértelmezett érték a tartomány alapértelmezett SZERVEZETIEGYSÉG-objektuma.</span><span class="sxs-lookup"><span data-stu-id="5fa48-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="5fa48-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fa48-138">-ResourceGroupName</span></span>
<span data-ttu-id="5fa48-139">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fa48-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5fa48-140">– Újraindítás</span><span class="sxs-lookup"><span data-stu-id="5fa48-140">-Restart</span></span>
<span data-ttu-id="5fa48-141">Jelzi, hogy ez a parancsmag újra elindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="5fa48-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="5fa48-142">A módosítások érvénybe léptetéséhez gyakran szükséges újraindítást végezni.</span><span class="sxs-lookup"><span data-stu-id="5fa48-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="5fa48-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5fa48-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="5fa48-144">A tartomány kiterjesztésének verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fa48-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="5fa48-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="5fa48-145">-VMName</span></span>
<span data-ttu-id="5fa48-146">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fa48-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="5fa48-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5fa48-147">-Confirm</span></span>
<span data-ttu-id="5fa48-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5fa48-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fa48-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fa48-149">-WhatIf</span></span>
<span data-ttu-id="5fa48-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5fa48-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fa48-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fa48-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fa48-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fa48-152">CommonParameters</span></span>
<span data-ttu-id="5fa48-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fa48-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fa48-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5fa48-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fa48-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fa48-155">INPUTS</span></span>

### <span data-ttu-id="5fa48-156">System. String</span><span class="sxs-lookup"><span data-stu-id="5fa48-156">System.String</span></span>

### <span data-ttu-id="5fa48-157">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5fa48-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5fa48-158">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="5fa48-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="5fa48-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5fa48-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5fa48-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fa48-160">OUTPUTS</span></span>

### <span data-ttu-id="5fa48-161">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5fa48-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5fa48-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fa48-162">NOTES</span></span>

## <span data-ttu-id="5fa48-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fa48-163">RELATED LINKS</span></span>

[<span data-ttu-id="5fa48-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5fa48-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
