---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e0d36e8ddc239d1d075b79e0c91df645d671c6a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504460"
---
# <span data-ttu-id="cb2e7-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="cb2e7-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="cb2e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2e7-103">AD tartomány-kiterjesztést ad egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb2e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb2e7-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb2e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb2e7-105">DESCRIPTION</span></span>
<span data-ttu-id="cb2e7-106">A **set-AzureRmVMADDomainExtension** parancsmag hozzáadja az Azure Active Directory (ad) domain Virtual Machine bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="cb2e7-107">Ez a kiterjesztés lehetővé teszi, hogy a virtuális gép csatlakozzon a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="cb2e7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cb2e7-108">EXAMPLES</span></span>

## <span data-ttu-id="cb2e7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb2e7-109">PARAMETERS</span></span>

### <span data-ttu-id="cb2e7-110">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="cb2e7-110">-Credential</span></span>
<span data-ttu-id="cb2e7-111">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="cb2e7-112">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="cb2e7-113">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="cb2e7-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="cb2e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2e7-114">-DefaultProfile</span></span>
<span data-ttu-id="cb2e7-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb2e7-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cb2e7-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="cb2e7-117">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="cb2e7-118">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="cb2e7-118">-DomainName</span></span>
<span data-ttu-id="cb2e7-119">A tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="cb2e7-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="cb2e7-120">-ForceRerun</span></span>
<span data-ttu-id="cb2e7-121">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="cb2e7-122">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="cb2e7-123">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="cb2e7-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="cb2e7-124">-JoinOption</span></span>
<span data-ttu-id="cb2e7-125">A csatlakozás lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-125">Specifies the join option.</span></span> <span data-ttu-id="cb2e7-126">Csatlakozás beállításai lásd: [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="cb2e7-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="cb2e7-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="cb2e7-127">-Location</span></span>
<span data-ttu-id="cb2e7-128">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="cb2e7-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb2e7-129">-Name</span></span>
<span data-ttu-id="cb2e7-130">Annak a tartománynak a nevét adja meg, amelybe fel szeretné venni a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="cb2e7-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="cb2e7-131">-OUPath</span></span>
<span data-ttu-id="cb2e7-132">A tartományi fiókhoz tartozó szervezeti egység (OU) meghatározása.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="cb2e7-133">Adja meg a szervezeti egység teljes megkülönböztető nevét idézőjelek között.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="cb2e7-134">Az alapértelmezett érték a tartomány alapértelmezett SZERVEZETIEGYSÉG-objektuma.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-134">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="cb2e7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb2e7-135">-ResourceGroupName</span></span>
<span data-ttu-id="cb2e7-136">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cb2e7-137">– Újraindítás</span><span class="sxs-lookup"><span data-stu-id="cb2e7-137">-Restart</span></span>
<span data-ttu-id="cb2e7-138">Jelzi, hogy ez a parancsmag újra elindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="cb2e7-139">A módosítások érvénybe léptetéséhez gyakran szükséges újraindítást végezni.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-139">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="cb2e7-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cb2e7-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="cb2e7-141">A tartomány kiterjesztésének verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-141">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="cb2e7-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="cb2e7-142">-VMName</span></span>
<span data-ttu-id="cb2e7-143">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-143">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="cb2e7-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb2e7-144">-Confirm</span></span>
<span data-ttu-id="cb2e7-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2e7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2e7-146">-WhatIf</span></span>
<span data-ttu-id="cb2e7-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb2e7-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2e7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2e7-149">CommonParameters</span></span>
<span data-ttu-id="cb2e7-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb2e7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2e7-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2e7-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2e7-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2e7-152">INPUTS</span></span>

### <span data-ttu-id="cb2e7-153">System. String</span><span class="sxs-lookup"><span data-stu-id="cb2e7-153">System.String</span></span>

### <span data-ttu-id="cb2e7-154">System. null ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cb2e7-154">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="cb2e7-155">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="cb2e7-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="cb2e7-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cb2e7-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cb2e7-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2e7-157">OUTPUTS</span></span>

### <span data-ttu-id="cb2e7-158">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cb2e7-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cb2e7-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb2e7-159">NOTES</span></span>

## <span data-ttu-id="cb2e7-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb2e7-160">RELATED LINKS</span></span>

[<span data-ttu-id="cb2e7-161">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="cb2e7-161">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
