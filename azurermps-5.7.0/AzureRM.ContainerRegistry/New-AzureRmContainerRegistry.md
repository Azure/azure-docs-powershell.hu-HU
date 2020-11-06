---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: ce72af78fec87182e1061259cd0c0d51d9819767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493169"
---
# <span data-ttu-id="5262a-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5262a-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="5262a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5262a-102">SYNOPSIS</span></span>
<span data-ttu-id="5262a-103">Tároló-nyilvántartót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5262a-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5262a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5262a-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5262a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5262a-105">DESCRIPTION</span></span>
<span data-ttu-id="5262a-106">Az New-AzureRmContainerRegistry parancsmag létrehoz egy tároló-nyilvántartót.</span><span class="sxs-lookup"><span data-stu-id="5262a-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="5262a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5262a-107">EXAMPLES</span></span>

### <span data-ttu-id="5262a-108">1. példa: új tárterület-fiók létrehozása a tároló beállításjegyzékben.</span><span class="sxs-lookup"><span data-stu-id="5262a-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="5262a-109">Ez a parancs létrehoz egy tároló beállításjegyzéket egy új tárterület-fiókkal az erőforráscsoport \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="5262a-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="5262a-110">2. példa: a tároló beállításjegyzékének létrehozása engedélyezve van a rendszergazdai felhasználóval.</span><span class="sxs-lookup"><span data-stu-id="5262a-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="5262a-111">Ez a parancs létrehoz egy tároló beállításjegyzéket, amelyben engedélyezve van a rendszergazdai felhasználó.</span><span class="sxs-lookup"><span data-stu-id="5262a-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="5262a-112">3. példa: a tároló beállításjegyzékének létrehozása meglévő tárterület-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="5262a-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="5262a-113">Ez a parancs létrehoz egy tároló beállításjegyzéket egy meglévő tárterület \` -mystorageaccount az \` előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="5262a-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="5262a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5262a-114">PARAMETERS</span></span>

### <span data-ttu-id="5262a-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="5262a-115">-EnableAdminUser</span></span>
<span data-ttu-id="5262a-116">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="5262a-116">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5262a-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="5262a-117">-Location</span></span>
<span data-ttu-id="5262a-118">A tároló beállításjegyzékének helye.</span><span class="sxs-lookup"><span data-stu-id="5262a-118">Container Registry Location.</span></span>
<span data-ttu-id="5262a-119">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="5262a-119">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5262a-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5262a-120">-Name</span></span>
<span data-ttu-id="5262a-121">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="5262a-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5262a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5262a-122">-ResourceGroupName</span></span>
<span data-ttu-id="5262a-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5262a-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5262a-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="5262a-124">-Sku</span></span>
<span data-ttu-id="5262a-125">Tároló rendszerleíró SKU (SKU)</span><span class="sxs-lookup"><span data-stu-id="5262a-125">Container Registry SKU.</span></span>
<span data-ttu-id="5262a-126">Engedélyezett értékek: egyszerű.</span><span class="sxs-lookup"><span data-stu-id="5262a-126">Allowed values: Basic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5262a-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5262a-127">-StorageAccountName</span></span>
<span data-ttu-id="5262a-128">Egy meglévő tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="5262a-128">The name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5262a-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="5262a-129">-Tag</span></span>
<span data-ttu-id="5262a-130">Tároló rendszerleíróadatbázis-címkék. kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="5262a-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="5262a-131">Példa:</span><span class="sxs-lookup"><span data-stu-id="5262a-131">For example:</span></span>

<span data-ttu-id="5262a-132">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="5262a-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5262a-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5262a-133">-Confirm</span></span>
<span data-ttu-id="5262a-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5262a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5262a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5262a-135">-WhatIf</span></span>
<span data-ttu-id="5262a-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5262a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5262a-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5262a-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5262a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5262a-138">-DefaultProfile</span></span>
<span data-ttu-id="5262a-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5262a-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5262a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5262a-140">CommonParameters</span></span>
<span data-ttu-id="5262a-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5262a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5262a-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5262a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5262a-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5262a-143">INPUTS</span></span>

### <span data-ttu-id="5262a-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="5262a-144">None</span></span>
<span data-ttu-id="5262a-145">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5262a-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5262a-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5262a-146">OUTPUTS</span></span>

### <span data-ttu-id="5262a-147">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5262a-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="5262a-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5262a-148">NOTES</span></span>

## <span data-ttu-id="5262a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5262a-149">RELATED LINKS</span></span>

[<span data-ttu-id="5262a-150">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5262a-150">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="5262a-151">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5262a-151">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="5262a-152">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5262a-152">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

