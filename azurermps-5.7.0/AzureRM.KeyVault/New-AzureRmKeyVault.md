---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 7cc4af3e849a6cd24c2144c6e92c990da261e9d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679733"
---
# <span data-ttu-id="5af39-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="5af39-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="5af39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5af39-102">SYNOPSIS</span></span>
<span data-ttu-id="5af39-103">Egy fő boltozatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5af39-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5af39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5af39-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5af39-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5af39-105">DESCRIPTION</span></span>
<span data-ttu-id="5af39-106">A **New-AzureRmKeyVault** parancsmag létrehoz egy fő boltozatot a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="5af39-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="5af39-107">Ez a parancsmag az aktuálisan bejelentkezett felhasználó engedélyeit is feljogosítja a kulcsfájl hozzáadására, eltávolítására, illetve a kulcsok és a titok megadására.</span><span class="sxs-lookup"><span data-stu-id="5af39-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="5af39-108">Megjegyzés: Ha a hiba megjelenik, **az előfizetéshez nincs regisztrálva a "Microsoft. kulcskezelő" névtér használata** az új kulcsfájl létrehozásakor, futtassa a **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. kulcskezelő"** parancsot, majd futtassa újra a **New-AzureRmKeyVault** parancsot.</span><span class="sxs-lookup"><span data-stu-id="5af39-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="5af39-109">További információt a Register-AzureRmResourceProvider című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5af39-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="5af39-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5af39-110">EXAMPLES</span></span>

### <span data-ttu-id="5af39-111">Példa 1: normál kulcsú boltozat létrehozása</span><span class="sxs-lookup"><span data-stu-id="5af39-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="5af39-112">Ez a parancs létrehoz egy Contoso03Vault nevű kulcs boltozatot az Azure régióban, a Kelet-Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="5af39-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="5af39-113">A parancs hozzáadja a fő boltozatot a Group14 nevű erőforráscsoport csoportjához.</span><span class="sxs-lookup"><span data-stu-id="5af39-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="5af39-114">Mivel a parancs nem ad meg értéket a *SKU* paraméterhez, létrehoz egy standard kulcs boltozatot.</span><span class="sxs-lookup"><span data-stu-id="5af39-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="5af39-115">2. példa: prémium kulcsú boltozat létrehozása</span><span class="sxs-lookup"><span data-stu-id="5af39-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="5af39-116">Ez a parancs az előző példához hasonlóan létrehoz egy fő boltozatot.</span><span class="sxs-lookup"><span data-stu-id="5af39-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="5af39-117">A prémium kulcsú boltozatot azonban a *SKU* paraméterhez tartozó prémium értékkel adja meg.</span><span class="sxs-lookup"><span data-stu-id="5af39-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="5af39-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5af39-118">PARAMETERS</span></span>

### <span data-ttu-id="5af39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af39-119">-DefaultProfile</span></span>
<span data-ttu-id="5af39-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5af39-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="5af39-121">-EnabledForDeployment</span></span>
<span data-ttu-id="5af39-122">A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="5af39-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5af39-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="5af39-124">Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.</span><span class="sxs-lookup"><span data-stu-id="5af39-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="5af39-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="5af39-126">Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="5af39-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-127">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="5af39-127">-EnableSoftDelete</span></span>
<span data-ttu-id="5af39-128">Itt adhatja meg, hogy engedélyezve van-e a finom törlés funkció ehhez a kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="5af39-128">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="5af39-129">Ha a Soft-delete beállítás engedélyezve van, a türelmi időszakra visszaállíthatja a fő boltozatot és annak tartalmát a törlés után.</span><span class="sxs-lookup"><span data-stu-id="5af39-129">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>

<span data-ttu-id="5af39-130">A funkcióról további információt az [Azure Key Vault Soft-delete – áttekintés](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5af39-130">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="5af39-131">Útmutatásért olvassa el a következő témakört: [Hogyan lehet használni a kulcsfájl Soft-deletet a PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)segítségével.</span><span class="sxs-lookup"><span data-stu-id="5af39-131">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="5af39-132">-Location</span></span>
<span data-ttu-id="5af39-133">Azt az Azure-területet adja meg, amelyben a fő pince hozható létre.</span><span class="sxs-lookup"><span data-stu-id="5af39-133">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="5af39-134">Használja a [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) parancsot a lehetőségek megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="5af39-134">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5af39-135">-Name</span></span>
<span data-ttu-id="5af39-136">A létrehozandó fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5af39-136">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="5af39-137">A név lehet betűk, számjegyek és kötőjelek tetszőleges kombinációja.</span><span class="sxs-lookup"><span data-stu-id="5af39-137">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="5af39-138">A névnek betűvel vagy számmal kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="5af39-138">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="5af39-139">A névnek univerzálisan egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5af39-139">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af39-140">-ResourceGroupName</span></span>
<span data-ttu-id="5af39-141">Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="5af39-141">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="5af39-142">-Sku</span></span>
<span data-ttu-id="5af39-143">A fő boltozat-példány SKU-ának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="5af39-143">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="5af39-144">Ha tudni kívánja, hogy mely funkciók érhetők el az egyes SKU-hoz, olvassa el az Azure Key Vault árképzési webhelye című témakört https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="5af39-144">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="5af39-145">-Tag</span></span>
<span data-ttu-id="5af39-146">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="5af39-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5af39-147">Példa:</span><span class="sxs-lookup"><span data-stu-id="5af39-147">For example:</span></span>

<span data-ttu-id="5af39-148">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="5af39-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5af39-149">-Confirm</span></span>
<span data-ttu-id="5af39-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5af39-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af39-151">-WhatIf</span></span>
<span data-ttu-id="5af39-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5af39-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af39-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5af39-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5af39-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af39-154">CommonParameters</span></span>
<span data-ttu-id="5af39-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5af39-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af39-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af39-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af39-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5af39-157">INPUTS</span></span>

### <span data-ttu-id="5af39-158">Nincs</span><span class="sxs-lookup"><span data-stu-id="5af39-158">None</span></span>
<span data-ttu-id="5af39-159">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5af39-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5af39-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5af39-160">OUTPUTS</span></span>

### <span data-ttu-id="5af39-161">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="5af39-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="5af39-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5af39-162">NOTES</span></span>

## <span data-ttu-id="5af39-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5af39-163">RELATED LINKS</span></span>

[<span data-ttu-id="5af39-164">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="5af39-164">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="5af39-165">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="5af39-165">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
