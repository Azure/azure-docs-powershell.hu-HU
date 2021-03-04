---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 4d9b788637e0c97d8f129df33ac7e4050ce916d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924209"
---
# <span data-ttu-id="37150-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37150-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="37150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37150-102">SYNOPSIS</span></span>
<span data-ttu-id="37150-103">Létrehoz egy tárolóadatbázist.</span><span class="sxs-lookup"><span data-stu-id="37150-103">Creates a container registry.</span></span>

## <span data-ttu-id="37150-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37150-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37150-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37150-105">DESCRIPTION</span></span>
<span data-ttu-id="37150-106">A New-AzContainerRegistry parancsmag létrehoz egy tárolóadatbázist.</span><span class="sxs-lookup"><span data-stu-id="37150-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="37150-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37150-107">EXAMPLES</span></span>

### <span data-ttu-id="37150-108">1. példa: Hozzon létre egy új tárfiókot tartalmazó tárolóadatbázist.</span><span class="sxs-lookup"><span data-stu-id="37150-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="37150-109">Ez a parancs létrehoz egy új tárolóadatbázist a \` MyResourceGroup \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="37150-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="37150-110">2. példa: Tároló beállításjegyzékének létrehozása engedélyezett rendszergazdai felhasználóval.</span><span class="sxs-lookup"><span data-stu-id="37150-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="37150-111">Ez a parancs létrehoz egy tárolóadatbázist úgy, hogy a rendszergazdai felhasználó engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="37150-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="37150-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37150-112">PARAMETERS</span></span>

### <span data-ttu-id="37150-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37150-113">-DefaultProfile</span></span>
<span data-ttu-id="37150-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="37150-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37150-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="37150-115">-EnableAdminUser</span></span>
<span data-ttu-id="37150-116">Engedélyezze a rendszergazdai felhasználót a tároló beállításjegyzékéhez.</span><span class="sxs-lookup"><span data-stu-id="37150-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="37150-117">-Location</span><span class="sxs-lookup"><span data-stu-id="37150-117">-Location</span></span>
<span data-ttu-id="37150-118">Container Registry Location.</span><span class="sxs-lookup"><span data-stu-id="37150-118">Container Registry Location.</span></span>
<span data-ttu-id="37150-119">Alapértelmezés szerint az erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="37150-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="37150-120">-Name</span><span class="sxs-lookup"><span data-stu-id="37150-120">-Name</span></span>
<span data-ttu-id="37150-121">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="37150-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="37150-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37150-122">-ResourceGroupName</span></span>
<span data-ttu-id="37150-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="37150-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="37150-124">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="37150-124">-Sku</span></span>
<span data-ttu-id="37150-125">Container Registry termékváltozat.</span><span class="sxs-lookup"><span data-stu-id="37150-125">Container Registry SKU.</span></span>
<span data-ttu-id="37150-126">Engedélyezett értékek: Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="37150-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="37150-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="37150-127">-Tag</span></span>
<span data-ttu-id="37150-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span><span class="sxs-lookup"><span data-stu-id="37150-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="37150-129">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="37150-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="37150-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37150-130">-Confirm</span></span>
<span data-ttu-id="37150-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="37150-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37150-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37150-132">-WhatIf</span></span>
<span data-ttu-id="37150-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="37150-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37150-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37150-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37150-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37150-135">CommonParameters</span></span>
<span data-ttu-id="37150-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37150-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37150-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37150-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37150-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37150-138">INPUTS</span></span>

### <span data-ttu-id="37150-139">System.String</span><span class="sxs-lookup"><span data-stu-id="37150-139">System.String</span></span>

## <span data-ttu-id="37150-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37150-140">OUTPUTS</span></span>

### <span data-ttu-id="37150-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37150-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="37150-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37150-142">NOTES</span></span>

## <span data-ttu-id="37150-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37150-143">RELATED LINKS</span></span>

[<span data-ttu-id="37150-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37150-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="37150-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37150-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="37150-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37150-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

