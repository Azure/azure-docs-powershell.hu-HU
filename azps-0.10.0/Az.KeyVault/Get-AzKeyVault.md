---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: aaace602cd50f9464021b1dcbefe39272e1621bb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842162"
---
# <span data-ttu-id="fe31d-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe31d-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="fe31d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe31d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe31d-103">Kulcsos boltozatokat kap.</span><span class="sxs-lookup"><span data-stu-id="fe31d-103">Gets key vaults.</span></span>

## <span data-ttu-id="fe31d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe31d-104">SYNTAX</span></span>

### <span data-ttu-id="fe31d-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="fe31d-105">GetVaultByName</span></span>
```
Get-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe31d-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="fe31d-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe31d-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe31d-107">ListVaultsByResourceGroup</span></span>
```
Get-AzKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe31d-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="fe31d-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe31d-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="fe31d-109">ListAllVaultsInSubscription</span></span>
```
Get-AzKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe31d-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe31d-110">DESCRIPTION</span></span>
<span data-ttu-id="fe31d-111">A **Get-AzKeyVault** parancsmag információkat kap az előfizetések fő boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="fe31d-111">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="fe31d-112">Az előfizetésben megtekintheti az összes fontos boltozat-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott kulcs boltozatával.</span><span class="sxs-lookup"><span data-stu-id="fe31d-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="fe31d-113">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező a parancsmag számára, ha egyetlen kulcs típusú boltozatot kap, akkor a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="fe31d-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="fe31d-114">Példák</span><span class="sxs-lookup"><span data-stu-id="fe31d-114">EXAMPLES</span></span>

### <span data-ttu-id="fe31d-115">Példa 1: a jelenlegi előfizetésben lévő összes kulcs boltozatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fe31d-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault
```

<span data-ttu-id="fe31d-116">Ez a parancs a jelenlegi előfizetésben a legfontosabb boltozatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="fe31d-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="fe31d-117">2. példa: adott kulcsos boltozat beszerzése</span><span class="sxs-lookup"><span data-stu-id="fe31d-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="fe31d-118">Ez a parancs a Contoso03Vault nevű kulcs boltozatát kapja a jelenlegi előfizetésben, majd a $MyVault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe31d-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="fe31d-119">A $MyVault tulajdonságait ellenőrizheti, hogy miként kaphat részleteket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="fe31d-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="fe31d-120">3. példa: kulcsos boltívek beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="fe31d-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="fe31d-121">Ez a parancs a ContosoPayRollResourceGroup nevű erőforráscsoport minden fő boltozatát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="fe31d-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="fe31d-122">4. példa: az összes törölt kulcsfájl beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="fe31d-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault -InRemovedState
```

<span data-ttu-id="fe31d-123">Ez a parancs beolvassa a jelenlegi előfizetés összes törölt kulcsát.</span><span class="sxs-lookup"><span data-stu-id="fe31d-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="fe31d-124">Példa 5: törölt kulcsfájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="fe31d-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="fe31d-125">Ez a parancs beolvassa a Contoso03Vault nevű, az aktuális előfizetésben és a eastus2-régióban a törölt kulcs boltozattal kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="fe31d-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="fe31d-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe31d-126">PARAMETERS</span></span>

### <span data-ttu-id="fe31d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe31d-127">-DefaultProfile</span></span>
<span data-ttu-id="fe31d-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fe31d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe31d-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fe31d-129">-InRemovedState</span></span>
<span data-ttu-id="fe31d-130">Itt adhatja meg, hogy megjelenjen-e a korábban törölt boltozatok a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="fe31d-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="fe31d-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="fe31d-131">-Location</span></span>
<span data-ttu-id="fe31d-132">A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="fe31d-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe31d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe31d-133">-ResourceGroupName</span></span>
<span data-ttu-id="fe31d-134">A lekérdezett fő boltozattal vagy a fő boltozatokkal társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe31d-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe31d-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="fe31d-135">-Tag</span></span>
<span data-ttu-id="fe31d-136">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fe31d-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe31d-137">Példa:</span><span class="sxs-lookup"><span data-stu-id="fe31d-137">For example:</span></span>

<span data-ttu-id="fe31d-138">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="fe31d-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fe31d-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fe31d-139">-VaultName</span></span>
<span data-ttu-id="fe31d-140">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe31d-140">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe31d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe31d-141">CommonParameters</span></span>
<span data-ttu-id="fe31d-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe31d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe31d-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe31d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe31d-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe31d-144">INPUTS</span></span>

### <span data-ttu-id="fe31d-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe31d-145">None</span></span>
<span data-ttu-id="fe31d-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fe31d-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe31d-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe31d-147">OUTPUTS</span></span>

### <span data-ttu-id="fe31d-148">Microsoft. Azure. Command. PSVault. models.</span><span class="sxs-lookup"><span data-stu-id="fe31d-148">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="fe31d-149">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. devault. models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="fe31d-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="fe31d-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="fe31d-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="fe31d-151">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="fe31d-151">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="fe31d-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe31d-152">NOTES</span></span>

## <span data-ttu-id="fe31d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe31d-153">RELATED LINKS</span></span>

[<span data-ttu-id="fe31d-154">Új – AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe31d-154">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="fe31d-155">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe31d-155">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
