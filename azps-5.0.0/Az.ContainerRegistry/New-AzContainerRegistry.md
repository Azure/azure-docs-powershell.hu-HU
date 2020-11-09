---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296387"
---
# <span data-ttu-id="b73a2-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b73a2-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="b73a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b73a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b73a2-103">Tároló-nyilvántartót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b73a2-103">Creates a container registry.</span></span>

## <span data-ttu-id="b73a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b73a2-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b73a2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b73a2-105">DESCRIPTION</span></span>
<span data-ttu-id="b73a2-106">Az New-AzContainerRegistry parancsmag létrehoz egy tároló-nyilvántartót.</span><span class="sxs-lookup"><span data-stu-id="b73a2-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="b73a2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b73a2-107">EXAMPLES</span></span>

### <span data-ttu-id="b73a2-108">1. példa: új tárterület-fiók létrehozása a tároló beállításjegyzékben.</span><span class="sxs-lookup"><span data-stu-id="b73a2-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="b73a2-109">Ez a parancs létrehoz egy tároló beállításjegyzéket egy új tárterület-fiókkal az erőforráscsoport \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="b73a2-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="b73a2-110">2. példa: a tároló beállításjegyzékének létrehozása engedélyezve van a rendszergazdai felhasználóval.</span><span class="sxs-lookup"><span data-stu-id="b73a2-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="b73a2-111">Ez a parancs létrehoz egy tároló beállításjegyzéket, amelyben engedélyezve van a rendszergazdai felhasználó.</span><span class="sxs-lookup"><span data-stu-id="b73a2-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="b73a2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b73a2-112">PARAMETERS</span></span>

### <span data-ttu-id="b73a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73a2-113">-DefaultProfile</span></span>
<span data-ttu-id="b73a2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b73a2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b73a2-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="b73a2-115">-EnableAdminUser</span></span>
<span data-ttu-id="b73a2-116">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="b73a2-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="b73a2-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="b73a2-117">-Location</span></span>
<span data-ttu-id="b73a2-118">A tároló beállításjegyzékének helye.</span><span class="sxs-lookup"><span data-stu-id="b73a2-118">Container Registry Location.</span></span>
<span data-ttu-id="b73a2-119">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="b73a2-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="b73a2-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b73a2-120">-Name</span></span>
<span data-ttu-id="b73a2-121">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="b73a2-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="b73a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b73a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="b73a2-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b73a2-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="b73a2-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="b73a2-124">-Sku</span></span>
<span data-ttu-id="b73a2-125">Tároló rendszerleíró SKU (SKU)</span><span class="sxs-lookup"><span data-stu-id="b73a2-125">Container Registry SKU.</span></span>
<span data-ttu-id="b73a2-126">Engedélyezett értékek: egyszerű.</span><span class="sxs-lookup"><span data-stu-id="b73a2-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b73a2-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="b73a2-127">-Tag</span></span>
<span data-ttu-id="b73a2-128">Tároló rendszerleíróadatbázis-címkék. kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="b73a2-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="b73a2-129">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="b73a2-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b73a2-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b73a2-130">-Confirm</span></span>
<span data-ttu-id="b73a2-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b73a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b73a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b73a2-132">-WhatIf</span></span>
<span data-ttu-id="b73a2-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b73a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b73a2-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b73a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b73a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73a2-135">CommonParameters</span></span>
<span data-ttu-id="b73a2-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b73a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73a2-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b73a2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73a2-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b73a2-138">INPUTS</span></span>

### <span data-ttu-id="b73a2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b73a2-139">System.String</span></span>

## <span data-ttu-id="b73a2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b73a2-140">OUTPUTS</span></span>

### <span data-ttu-id="b73a2-141">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b73a2-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="b73a2-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b73a2-142">NOTES</span></span>

## <span data-ttu-id="b73a2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b73a2-143">RELATED LINKS</span></span>

[<span data-ttu-id="b73a2-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b73a2-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="b73a2-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b73a2-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="b73a2-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b73a2-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

