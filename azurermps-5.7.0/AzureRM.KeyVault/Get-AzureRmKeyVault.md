---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505507"
---
# <span data-ttu-id="9a127-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9a127-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="9a127-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a127-102">SYNOPSIS</span></span>
<span data-ttu-id="9a127-103">Kulcsos boltozatokat kap.</span><span class="sxs-lookup"><span data-stu-id="9a127-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a127-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a127-104">SYNTAX</span></span>

### <span data-ttu-id="9a127-105">ListAllVaultsInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a127-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a127-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="9a127-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a127-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="9a127-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a127-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="9a127-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a127-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a127-109">DESCRIPTION</span></span>
<span data-ttu-id="9a127-110">A **Get-AzureRmKeyVault** parancsmag információkat kap az előfizetések fő boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="9a127-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="9a127-111">Az előfizetésben megtekintheti az összes fontos boltozat-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott kulcs boltozatával.</span><span class="sxs-lookup"><span data-stu-id="9a127-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="9a127-112">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező a parancsmag számára, ha egyetlen kulcs típusú boltozatot kap, akkor a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="9a127-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="9a127-113">Példák</span><span class="sxs-lookup"><span data-stu-id="9a127-113">EXAMPLES</span></span>

### <span data-ttu-id="9a127-114">Példa 1: a jelenlegi előfizetésben lévő összes kulcs boltozatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9a127-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="9a127-115">Ez a parancs a jelenlegi előfizetésben a legfontosabb boltozatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="9a127-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="9a127-116">2. példa: adott kulcsos boltozat beszerzése</span><span class="sxs-lookup"><span data-stu-id="9a127-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="9a127-117">Ez a parancs a Contoso03Vault nevű kulcs boltozatát kapja a jelenlegi előfizetésben, majd a $MyVault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9a127-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="9a127-118">A $MyVault tulajdonságait ellenőrizheti, hogy miként kaphat részleteket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="9a127-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="9a127-119">3. példa: kulcsos boltívek beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="9a127-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="9a127-120">Ez a parancs a ContosoPayRollResourceGroup nevű erőforráscsoport minden fő boltozatát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="9a127-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="9a127-121">4. példa: az összes törölt kulcsfájl beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="9a127-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="9a127-122">Ez a parancs beolvassa a jelenlegi előfizetés összes törölt kulcsát.</span><span class="sxs-lookup"><span data-stu-id="9a127-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="9a127-123">Példa 5: törölt kulcsfájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="9a127-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="9a127-124">Ez a parancs beolvassa a Contoso03Vault nevű, az aktuális előfizetésben és a eastus2-régióban a törölt kulcs boltozattal kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="9a127-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="9a127-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a127-125">PARAMETERS</span></span>

### <span data-ttu-id="9a127-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a127-126">-DefaultProfile</span></span>
<span data-ttu-id="9a127-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9a127-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a127-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="9a127-128">-InRemovedState</span></span>
<span data-ttu-id="9a127-129">Itt adhatja meg, hogy megjelenjen-e a korábban törölt boltozatok a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="9a127-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a127-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="9a127-130">-Location</span></span>
<span data-ttu-id="9a127-131">A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="9a127-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a127-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a127-132">-ResourceGroupName</span></span>
<span data-ttu-id="9a127-133">A lekérdezett fő boltozattal vagy a fő boltozatokkal társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a127-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a127-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="9a127-134">-Tag</span></span>
<span data-ttu-id="9a127-135">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="9a127-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9a127-136">Példa:</span><span class="sxs-lookup"><span data-stu-id="9a127-136">For example:</span></span>

<span data-ttu-id="9a127-137">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="9a127-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a127-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9a127-138">-VaultName</span></span>
<span data-ttu-id="9a127-139">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a127-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a127-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a127-140">CommonParameters</span></span>
<span data-ttu-id="9a127-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a127-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a127-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a127-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a127-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a127-143">INPUTS</span></span>

### <span data-ttu-id="9a127-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="9a127-144">None</span></span>
<span data-ttu-id="9a127-145">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9a127-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a127-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a127-146">OUTPUTS</span></span>

### <span data-ttu-id="9a127-147">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="9a127-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9a127-148">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. devault. models. PSKeyVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="9a127-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="9a127-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="9a127-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="9a127-150">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span><span class="sxs-lookup"><span data-stu-id="9a127-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="9a127-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a127-151">NOTES</span></span>

## <span data-ttu-id="9a127-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a127-152">RELATED LINKS</span></span>

[<span data-ttu-id="9a127-153">Új – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9a127-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="9a127-154">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9a127-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
