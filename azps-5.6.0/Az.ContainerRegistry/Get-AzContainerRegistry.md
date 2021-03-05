---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 969e37173c487b2ed3ee4ab6dad5374208f5ff27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004453"
---
# <span data-ttu-id="8395b-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8395b-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="8395b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8395b-102">SYNOPSIS</span></span>
<span data-ttu-id="8395b-103">Tároló beállításjegyzéket kap.</span><span class="sxs-lookup"><span data-stu-id="8395b-103">Gets a container registry.</span></span>

## <span data-ttu-id="8395b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8395b-104">SYNTAX</span></span>

### <span data-ttu-id="8395b-105">ListRegistriesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8395b-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8395b-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8395b-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8395b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8395b-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8395b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8395b-108">DESCRIPTION</span></span>
<span data-ttu-id="8395b-109">A Get-AzContainerRegistry parancsmag kap egy megadott tárolóadatbázist vagy egy erőforráscsoport vagy az előfizetés összes tároló-beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="8395b-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="8395b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8395b-110">EXAMPLES</span></span>

### <span data-ttu-id="8395b-111">1. példa: A megadott tárolóadatbázis lekérte</span><span class="sxs-lookup"><span data-stu-id="8395b-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="8395b-112">Ez a parancs a megadott tárolóadatbázist kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8395b-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="8395b-113">2. példa: Az erőforráscsoport összes tároló-beállítási beállításának be szereznie</span><span class="sxs-lookup"><span data-stu-id="8395b-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="8395b-114">Ez a parancs egy erőforráscsoport összes tároló-beállítási beállítását beveszi.</span><span class="sxs-lookup"><span data-stu-id="8395b-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="8395b-115">3. példa: Az előfizetés összes tároló-beállítási szolgáltatásának be szereznie</span><span class="sxs-lookup"><span data-stu-id="8395b-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="8395b-116">Ez a parancs az előfizetés összes tároló-beállítását beveszi.</span><span class="sxs-lookup"><span data-stu-id="8395b-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="8395b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8395b-117">PARAMETERS</span></span>

### <span data-ttu-id="8395b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8395b-118">-DefaultProfile</span></span>
<span data-ttu-id="8395b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8395b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8395b-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="8395b-120">-IncludeDetail</span></span>
<span data-ttu-id="8395b-121">További részletek megjelenítése a tároló beállításjegyzékről.</span><span class="sxs-lookup"><span data-stu-id="8395b-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="8395b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8395b-122">-Name</span></span>
<span data-ttu-id="8395b-123">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="8395b-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="8395b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8395b-124">-ResourceGroupName</span></span>
<span data-ttu-id="8395b-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8395b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8395b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8395b-126">-ResourceId</span></span>
<span data-ttu-id="8395b-127">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8395b-127">The container registry resource id</span></span>

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

### <span data-ttu-id="8395b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8395b-128">CommonParameters</span></span>
<span data-ttu-id="8395b-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8395b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8395b-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8395b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8395b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8395b-131">INPUTS</span></span>

### <span data-ttu-id="8395b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8395b-132">System.String</span></span>

## <span data-ttu-id="8395b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8395b-133">OUTPUTS</span></span>

### <span data-ttu-id="8395b-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8395b-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="8395b-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8395b-135">NOTES</span></span>

## <span data-ttu-id="8395b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8395b-136">RELATED LINKS</span></span>

[<span data-ttu-id="8395b-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8395b-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="8395b-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8395b-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="8395b-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8395b-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

