---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://go.microsoft.com/fwlink/?LinkID=690161
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 9a4d3399dd19d7dfced4f695623eef2fe0dba29d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493493"
---
# <span data-ttu-id="3ba7f-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ba7f-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="3ba7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ba7f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba7f-103">Kulcsos boltozatokat kap.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ba7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ba7f-104">SYNTAX</span></span>

### <span data-ttu-id="3ba7f-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="3ba7f-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ba7f-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="3ba7f-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ba7f-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3ba7f-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ba7f-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="3ba7f-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ba7f-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="3ba7f-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ba7f-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ba7f-110">DESCRIPTION</span></span>
<span data-ttu-id="3ba7f-111">A **Get-AzureRmKeyVault** parancsmag információkat kap az előfizetések fő boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="3ba7f-112">Az előfizetésben megtekintheti az összes fontos boltozat-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott kulcs boltozatával.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="3ba7f-113">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező a parancsmag számára, ha egyetlen kulcs típusú boltozatot kap, akkor a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="3ba7f-114">Példák</span><span class="sxs-lookup"><span data-stu-id="3ba7f-114">EXAMPLES</span></span>

### <span data-ttu-id="3ba7f-115">Példa 1: a jelenlegi előfizetésben lévő összes kulcs boltozatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ba7f-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="3ba7f-116">Ez a parancs a jelenlegi előfizetésben a legfontosabb boltozatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="3ba7f-117">2. példa: adott kulcsos boltozat beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ba7f-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="3ba7f-118">Ez a parancs a Contoso03Vault nevű kulcs boltozatát kapja a jelenlegi előfizetésben, majd a $MyVault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="3ba7f-119">A $MyVault tulajdonságait ellenőrizheti, hogy miként kaphat részleteket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="3ba7f-120">3. példa: kulcsos boltívek beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="3ba7f-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="3ba7f-121">Ez a parancs a ContosoPayRollResourceGroup nevű erőforráscsoport minden fő boltozatát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="3ba7f-122">4. példa: az összes törölt kulcsfájl beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="3ba7f-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="3ba7f-123">Ez a parancs beolvassa a jelenlegi előfizetés összes törölt kulcsát.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="3ba7f-124">Példa 5: törölt kulcsfájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ba7f-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="3ba7f-125">Ez a parancs beolvassa a Contoso03Vault nevű, az aktuális előfizetésben és a eastus2-régióban a törölt kulcs boltozattal kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="3ba7f-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ba7f-126">PARAMETERS</span></span>

### <span data-ttu-id="3ba7f-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3ba7f-127">-InRemovedState</span></span>
<span data-ttu-id="3ba7f-128">Itt adhatja meg, hogy megjelenjen-e a korábban törölt boltozatok a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba7f-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="3ba7f-129">-Location</span></span>
<span data-ttu-id="3ba7f-130">A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-130">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba7f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ba7f-131">-ResourceGroupName</span></span>
<span data-ttu-id="3ba7f-132">A lekérdezett fő boltozattal vagy a fő boltozatokkal társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba7f-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="3ba7f-133">-Tag</span></span>
<span data-ttu-id="3ba7f-134">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3ba7f-135">Példa:</span><span class="sxs-lookup"><span data-stu-id="3ba7f-135">For example:</span></span>

<span data-ttu-id="3ba7f-136">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3ba7f-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba7f-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3ba7f-137">-VaultName</span></span>
<span data-ttu-id="3ba7f-138">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba7f-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba7f-139">-DefaultProfile</span></span>
<span data-ttu-id="3ba7f-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ba7f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba7f-141">CommonParameters</span></span>
<span data-ttu-id="3ba7f-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ba7f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba7f-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ba7f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba7f-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ba7f-144">INPUTS</span></span>

## <span data-ttu-id="3ba7f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ba7f-145">OUTPUTS</span></span>

### <span data-ttu-id="3ba7f-146">Microsoft. Azure. Command. PSVault. models.</span><span class="sxs-lookup"><span data-stu-id="3ba7f-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="3ba7f-147">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. devault. models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="3ba7f-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="3ba7f-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="3ba7f-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="3ba7f-149">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="3ba7f-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="3ba7f-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ba7f-150">NOTES</span></span>

## <span data-ttu-id="3ba7f-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ba7f-151">RELATED LINKS</span></span>

[<span data-ttu-id="3ba7f-152">Új – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ba7f-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="3ba7f-153">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ba7f-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
