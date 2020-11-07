---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: c7ba57be16d929ba3cfa67c1e1e69aad48b12769
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836581"
---
# <span data-ttu-id="05513-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05513-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="05513-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05513-102">SYNOPSIS</span></span>
<span data-ttu-id="05513-103">Tároló-nyilvántartót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="05513-103">Creates a container registry.</span></span>

## <span data-ttu-id="05513-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05513-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05513-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05513-105">DESCRIPTION</span></span>
<span data-ttu-id="05513-106">Az New-AzContainerRegistry parancsmag létrehoz egy tároló-nyilvántartót.</span><span class="sxs-lookup"><span data-stu-id="05513-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="05513-107">Példák</span><span class="sxs-lookup"><span data-stu-id="05513-107">EXAMPLES</span></span>

### <span data-ttu-id="05513-108">1. példa: új tárterület-fiók létrehozása a tároló beállításjegyzékben.</span><span class="sxs-lookup"><span data-stu-id="05513-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="05513-109">Ez a parancs létrehoz egy tároló beállításjegyzéket egy új tárterület-fiókkal az erőforráscsoport \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="05513-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="05513-110">2. példa: a tároló beállításjegyzékének létrehozása engedélyezve van a rendszergazdai felhasználóval.</span><span class="sxs-lookup"><span data-stu-id="05513-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="05513-111">Ez a parancs létrehoz egy tároló beállításjegyzéket, amelyben engedélyezve van a rendszergazdai felhasználó.</span><span class="sxs-lookup"><span data-stu-id="05513-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="05513-112">3. példa: a tároló beállításjegyzékének létrehozása meglévő tárterület-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="05513-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="05513-113">Ez a parancs létrehoz egy tároló beállításjegyzéket egy meglévő tárterület \` -mystorageaccount az \` előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="05513-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="05513-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05513-114">PARAMETERS</span></span>

### <span data-ttu-id="05513-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05513-115">-DefaultProfile</span></span>
<span data-ttu-id="05513-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="05513-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05513-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="05513-117">-EnableAdminUser</span></span>
<span data-ttu-id="05513-118">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="05513-118">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05513-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="05513-119">-Location</span></span>
<span data-ttu-id="05513-120">A tároló beállításjegyzékének helye.</span><span class="sxs-lookup"><span data-stu-id="05513-120">Container Registry Location.</span></span>
<span data-ttu-id="05513-121">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="05513-121">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05513-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05513-122">-Name</span></span>
<span data-ttu-id="05513-123">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="05513-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05513-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05513-124">-ResourceGroupName</span></span>
<span data-ttu-id="05513-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="05513-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="05513-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="05513-126">-Sku</span></span>
<span data-ttu-id="05513-127">Tároló rendszerleíró SKU (SKU)</span><span class="sxs-lookup"><span data-stu-id="05513-127">Container Registry SKU.</span></span>
<span data-ttu-id="05513-128">Engedélyezett értékek: egyszerű.</span><span class="sxs-lookup"><span data-stu-id="05513-128">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05513-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="05513-129">-StorageAccountName</span></span>
<span data-ttu-id="05513-130">Egy meglévő tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="05513-130">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05513-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="05513-131">-Tag</span></span>
<span data-ttu-id="05513-132">Tároló rendszerleíróadatbázis-címkék. kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="05513-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="05513-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="05513-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05513-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="05513-134">-Confirm</span></span>
<span data-ttu-id="05513-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="05513-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05513-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05513-136">-WhatIf</span></span>
<span data-ttu-id="05513-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="05513-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05513-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05513-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05513-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05513-139">CommonParameters</span></span>
<span data-ttu-id="05513-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05513-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05513-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05513-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05513-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05513-142">INPUTS</span></span>

### <span data-ttu-id="05513-143">System. String</span><span class="sxs-lookup"><span data-stu-id="05513-143">System.String</span></span>

## <span data-ttu-id="05513-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05513-144">OUTPUTS</span></span>

### <span data-ttu-id="05513-145">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05513-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="05513-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05513-146">NOTES</span></span>

## <span data-ttu-id="05513-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05513-147">RELATED LINKS</span></span>

[<span data-ttu-id="05513-148">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05513-148">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="05513-149">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05513-149">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="05513-150">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05513-150">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

