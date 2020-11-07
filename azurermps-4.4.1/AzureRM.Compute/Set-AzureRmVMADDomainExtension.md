---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 663363ae2da1c17a9797f25260fa5a0b891fa483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672062"
---
# <span data-ttu-id="2baeb-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2baeb-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="2baeb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2baeb-102">SYNOPSIS</span></span>
<span data-ttu-id="2baeb-103">AD tartomány-kiterjesztést ad egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="2baeb-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2baeb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2baeb-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2baeb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2baeb-105">DESCRIPTION</span></span>
<span data-ttu-id="2baeb-106">A **set-AzureRmVMADDomainExtension** parancsmag hozzáadja az Azure Active Directory (ad) domain Virtual Machine bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="2baeb-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="2baeb-107">Ez a kiterjesztés lehetővé teszi, hogy a virtuális gép csatlakozzon a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="2baeb-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="2baeb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2baeb-108">EXAMPLES</span></span>

## <span data-ttu-id="2baeb-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2baeb-109">PARAMETERS</span></span>

### <span data-ttu-id="2baeb-110">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="2baeb-110">-Credential</span></span>
<span data-ttu-id="2baeb-111">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2baeb-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="2baeb-112">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2baeb-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="2baeb-113">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="2baeb-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="2baeb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2baeb-114">-DefaultProfile</span></span>
<span data-ttu-id="2baeb-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2baeb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2baeb-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2baeb-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2baeb-117">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="2baeb-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="2baeb-118">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="2baeb-118">-DomainName</span></span>
<span data-ttu-id="2baeb-119">A tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2baeb-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="2baeb-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2baeb-120">-ForceRerun</span></span>
<span data-ttu-id="2baeb-121">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2baeb-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="2baeb-122">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="2baeb-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="2baeb-123">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="2baeb-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="2baeb-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="2baeb-124">-JoinOption</span></span>
<span data-ttu-id="2baeb-125">A csatlakozás lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="2baeb-125">Specifies the join option.</span></span>

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

### <span data-ttu-id="2baeb-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="2baeb-126">-Location</span></span>
<span data-ttu-id="2baeb-127">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2baeb-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2baeb-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2baeb-128">-Name</span></span>
<span data-ttu-id="2baeb-129">Annak a tartománynak a nevét adja meg, amelybe fel szeretné venni a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="2baeb-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="2baeb-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="2baeb-130">-OUPath</span></span>
<span data-ttu-id="2baeb-131">A tartományi fiókhoz tartozó szervezeti egység (OU) meghatározása.</span><span class="sxs-lookup"><span data-stu-id="2baeb-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="2baeb-132">Adja meg a szervezeti egység teljes megkülönböztető nevét idézőjelek között.</span><span class="sxs-lookup"><span data-stu-id="2baeb-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="2baeb-133">Az alapértelmezett érték a tartomány alapértelmezett SZERVEZETIEGYSÉG-objektuma.</span><span class="sxs-lookup"><span data-stu-id="2baeb-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="2baeb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2baeb-134">-ResourceGroupName</span></span>
<span data-ttu-id="2baeb-135">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2baeb-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2baeb-136">– Újraindítás</span><span class="sxs-lookup"><span data-stu-id="2baeb-136">-Restart</span></span>
<span data-ttu-id="2baeb-137">Jelzi, hogy ez a parancsmag újra elindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="2baeb-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="2baeb-138">A módosítások érvénybe léptetéséhez gyakran szükséges újraindítást végezni.</span><span class="sxs-lookup"><span data-stu-id="2baeb-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="2baeb-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2baeb-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="2baeb-140">A tartomány kiterjesztésének verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2baeb-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="2baeb-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="2baeb-141">-VMName</span></span>
<span data-ttu-id="2baeb-142">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2baeb-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="2baeb-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2baeb-143">-Confirm</span></span>
<span data-ttu-id="2baeb-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2baeb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2baeb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2baeb-145">-WhatIf</span></span>
<span data-ttu-id="2baeb-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2baeb-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2baeb-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2baeb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2baeb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2baeb-148">CommonParameters</span></span>
<span data-ttu-id="2baeb-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2baeb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2baeb-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2baeb-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2baeb-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2baeb-151">INPUTS</span></span>

## <span data-ttu-id="2baeb-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2baeb-152">OUTPUTS</span></span>

## <span data-ttu-id="2baeb-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2baeb-153">NOTES</span></span>

## <span data-ttu-id="2baeb-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2baeb-154">RELATED LINKS</span></span>

[<span data-ttu-id="2baeb-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2baeb-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
