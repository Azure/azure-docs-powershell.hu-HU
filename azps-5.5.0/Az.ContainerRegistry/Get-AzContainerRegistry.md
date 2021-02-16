---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 759bc79a7ab36f99e01ce1e96b0bb6c3c6a9483b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148715"
---
# <span data-ttu-id="916c3-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="916c3-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="916c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="916c3-102">SYNOPSIS</span></span>
<span data-ttu-id="916c3-103">Tároló beállításjegyzéket kap.</span><span class="sxs-lookup"><span data-stu-id="916c3-103">Gets a container registry.</span></span>

## <span data-ttu-id="916c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="916c3-104">SYNTAX</span></span>

### <span data-ttu-id="916c3-105">ListRegistriesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="916c3-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="916c3-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="916c3-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="916c3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="916c3-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="916c3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="916c3-108">DESCRIPTION</span></span>
<span data-ttu-id="916c3-109">A Get-AzContainerRegistry parancsmag kap egy megadott tárolóadatbázist vagy egy erőforráscsoport vagy az előfizetés összes tároló-beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="916c3-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="916c3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="916c3-110">EXAMPLES</span></span>

### <span data-ttu-id="916c3-111">1. példa: A megadott tárolóadatbázis lekérte</span><span class="sxs-lookup"><span data-stu-id="916c3-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="916c3-112">Ez a parancs a megadott tárolóadatbázist kapja meg.</span><span class="sxs-lookup"><span data-stu-id="916c3-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="916c3-113">2. példa: Az erőforráscsoport összes tároló-beállítási beállításának be szereznie</span><span class="sxs-lookup"><span data-stu-id="916c3-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="916c3-114">Ez a parancs egy erőforráscsoport összes tároló-beállítási beállítását beveszi.</span><span class="sxs-lookup"><span data-stu-id="916c3-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="916c3-115">3. példa: Az előfizetés összes tároló-beállítási szolgáltatásának be szereznie</span><span class="sxs-lookup"><span data-stu-id="916c3-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="916c3-116">Ez a parancs az előfizetés összes tároló-beállítási szolgáltatását beveszi.</span><span class="sxs-lookup"><span data-stu-id="916c3-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="916c3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="916c3-117">PARAMETERS</span></span>

### <span data-ttu-id="916c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="916c3-118">-DefaultProfile</span></span>
<span data-ttu-id="916c3-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="916c3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="916c3-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="916c3-120">-IncludeDetail</span></span>
<span data-ttu-id="916c3-121">További részletek megjelenítése a tároló beállításjegyzékről.</span><span class="sxs-lookup"><span data-stu-id="916c3-121">Show more details about the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="916c3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="916c3-122">-Name</span></span>
<span data-ttu-id="916c3-123">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="916c3-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="916c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="916c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="916c3-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="916c3-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="916c3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="916c3-126">-ResourceId</span></span>
<span data-ttu-id="916c3-127">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="916c3-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="916c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="916c3-128">CommonParameters</span></span>
<span data-ttu-id="916c3-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="916c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="916c3-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="916c3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="916c3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="916c3-131">INPUTS</span></span>

### <span data-ttu-id="916c3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="916c3-132">System.String</span></span>

## <span data-ttu-id="916c3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="916c3-133">OUTPUTS</span></span>

### <span data-ttu-id="916c3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="916c3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="916c3-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="916c3-135">NOTES</span></span>

## <span data-ttu-id="916c3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="916c3-136">RELATED LINKS</span></span>

[<span data-ttu-id="916c3-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="916c3-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="916c3-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="916c3-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="916c3-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="916c3-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

