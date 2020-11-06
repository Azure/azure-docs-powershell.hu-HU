---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://go.microsoft.com/fwlink/?LinkId=690160
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 28cd93fe9de14365e4de626729ec45a7aaa88cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504923"
---
# <span data-ttu-id="fef13-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fef13-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="fef13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fef13-102">SYNOPSIS</span></span>
<span data-ttu-id="fef13-103">Egy fő boltozatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fef13-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fef13-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fef13-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fef13-105">DESCRIPTION</span></span>
<span data-ttu-id="fef13-106">A **New-AzureRmKeyVault** parancsmag létrehoz egy fő boltozatot a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="fef13-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="fef13-107">Ez a parancsmag az aktuálisan bejelentkezett felhasználó engedélyeit is feljogosítja a kulcsfájl hozzáadására, eltávolítására, illetve a kulcsok és a titok megadására.</span><span class="sxs-lookup"><span data-stu-id="fef13-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="fef13-108">Megjegyzés: Ha a hiba megjelenik, **az előfizetéshez nincs regisztrálva a "Microsoft. kulcskezelő" névtér használata** az új kulcsfájl létrehozásakor, futtassa a **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. kulcskezelő"** parancsot, majd futtassa újra a **New-AzureRmKeyVault** parancsot.</span><span class="sxs-lookup"><span data-stu-id="fef13-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="fef13-109">További információt a Register-AzureRmResourceProvider című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fef13-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="fef13-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fef13-110">EXAMPLES</span></span>

### <span data-ttu-id="fef13-111">Példa 1: normál kulcsú boltozat létrehozása</span><span class="sxs-lookup"><span data-stu-id="fef13-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="fef13-112">Ez a parancs létrehoz egy Contoso03Vault nevű kulcs boltozatot az Azure régióban, a Kelet-Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="fef13-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="fef13-113">A parancs hozzáadja a fő boltozatot a Group14 nevű erőforráscsoport csoportjához.</span><span class="sxs-lookup"><span data-stu-id="fef13-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="fef13-114">Mivel a parancs nem ad meg értéket a *SKU* paraméterhez, létrehoz egy standard kulcs boltozatot.</span><span class="sxs-lookup"><span data-stu-id="fef13-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="fef13-115">2. példa: prémium kulcsú boltozat létrehozása</span><span class="sxs-lookup"><span data-stu-id="fef13-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="fef13-116">Ez a parancs az előző példához hasonlóan létrehoz egy fő boltozatot.</span><span class="sxs-lookup"><span data-stu-id="fef13-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="fef13-117">A prémium kulcsú boltozatot azonban a *SKU* paraméterhez tartozó prémium értékkel adja meg.</span><span class="sxs-lookup"><span data-stu-id="fef13-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="fef13-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fef13-118">PARAMETERS</span></span>

### <span data-ttu-id="fef13-119">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="fef13-119">-EnabledForDeployment</span></span>
<span data-ttu-id="fef13-120">A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="fef13-120">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="fef13-121">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fef13-121">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="fef13-122">Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.</span><span class="sxs-lookup"><span data-stu-id="fef13-122">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="fef13-123">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="fef13-123">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="fef13-124">Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="fef13-124">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="fef13-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="fef13-125">-EnableSoftDelete</span></span>
<span data-ttu-id="fef13-126">Ha meg van adva, akkor a "puha Törlés" funkció engedélyezve van ehhez a kulcs boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="fef13-126">If specified, 'soft delete' functionality is enabled for this key vault.</span></span>

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

### <span data-ttu-id="fef13-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="fef13-127">-Location</span></span>
<span data-ttu-id="fef13-128">Azt az Azure-területet adja meg, amelyben a fő pince hozható létre.</span><span class="sxs-lookup"><span data-stu-id="fef13-128">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="fef13-129">A https://msdn.microsoft.com/ választható lehetőségek megjelenítéséhez használja az Get-AzureLocation (Library/Azure/mt589064. aspx) parancsot.</span><span class="sxs-lookup"><span data-stu-id="fef13-129">Use the command Get-AzureLocation (https://msdn.microsoft.com/ library/azure/mt589064.aspx) to see your choices.</span></span> <span data-ttu-id="fef13-130">További információért írja be a következőt: `Get-Help Get-AzureLocation` .</span><span class="sxs-lookup"><span data-stu-id="fef13-130">For more information, type `Get-Help Get-AzureLocation`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef13-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef13-131">-ResourceGroupName</span></span>
<span data-ttu-id="fef13-132">Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="fef13-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef13-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="fef13-133">-Sku</span></span>
<span data-ttu-id="fef13-134">A fő boltozat-példány SKU-ának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="fef13-134">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="fef13-135">Ha tudni kívánja, hogy mely funkciók érhetők el az egyes SKU-hoz, olvassa el az Azure Key Vault árképzési webhelye című témakört https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="fef13-135">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef13-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="fef13-136">-Tag</span></span>
<span data-ttu-id="fef13-137">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fef13-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fef13-138">Példa:</span><span class="sxs-lookup"><span data-stu-id="fef13-138">For example:</span></span>

<span data-ttu-id="fef13-139">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="fef13-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef13-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fef13-140">-VaultName</span></span>
<span data-ttu-id="fef13-141">A létrehozandó fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fef13-141">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="fef13-142">A név lehet betűk, számjegyek és kötőjelek tetszőleges kombinációja.</span><span class="sxs-lookup"><span data-stu-id="fef13-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="fef13-143">A névnek betűvel vagy számmal kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="fef13-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="fef13-144">A névnek univerzálisan egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fef13-144">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef13-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fef13-145">-Confirm</span></span>
<span data-ttu-id="fef13-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fef13-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fef13-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef13-147">-WhatIf</span></span>
<span data-ttu-id="fef13-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fef13-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fef13-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fef13-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fef13-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef13-150">-DefaultProfile</span></span>
<span data-ttu-id="fef13-151">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fef13-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fef13-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef13-152">CommonParameters</span></span>
<span data-ttu-id="fef13-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fef13-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef13-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef13-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef13-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fef13-155">INPUTS</span></span>

## <span data-ttu-id="fef13-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fef13-156">OUTPUTS</span></span>

### <span data-ttu-id="fef13-157">Microsoft. Azure. Command. PSVault. models.</span><span class="sxs-lookup"><span data-stu-id="fef13-157">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="fef13-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fef13-158">NOTES</span></span>

## <span data-ttu-id="fef13-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fef13-159">RELATED LINKS</span></span>

[<span data-ttu-id="fef13-160">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fef13-160">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="fef13-161">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fef13-161">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
