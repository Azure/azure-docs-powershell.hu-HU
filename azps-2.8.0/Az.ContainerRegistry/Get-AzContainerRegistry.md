---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: f833d2f46c67964356f48a06c35d41dfcf090fdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667135"
---
# <span data-ttu-id="97cb9-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97cb9-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="97cb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="97cb9-103">Tároló-nyilvántartót kap.</span><span class="sxs-lookup"><span data-stu-id="97cb9-103">Gets a container registry.</span></span>

## <span data-ttu-id="97cb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97cb9-104">SYNTAX</span></span>

### <span data-ttu-id="97cb9-105">ListRegistriesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97cb9-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97cb9-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="97cb9-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97cb9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97cb9-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97cb9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="97cb9-108">DESCRIPTION</span></span>
<span data-ttu-id="97cb9-109">A Get-AzContainerRegistry parancsmag egy adott tároló rendszerleíró adatbázisát vagy egy erőforráscsoport összes tároló-nyilvántartását, illetve az előfizetést kapja meg.</span><span class="sxs-lookup"><span data-stu-id="97cb9-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="97cb9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="97cb9-110">EXAMPLES</span></span>

### <span data-ttu-id="97cb9-111">1. példa: a megadott tároló beállításjegyzékének beszerzése</span><span class="sxs-lookup"><span data-stu-id="97cb9-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="97cb9-112">Ez a parancs a megadott tároló beállításjegyzékét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="97cb9-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="97cb9-113">2. példa: egy erőforráscsoport összes tároló-nyilvántartásának lekérése</span><span class="sxs-lookup"><span data-stu-id="97cb9-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="97cb9-114">Ez a parancs egy erőforráscsoport minden tároló-nyilvántartását beolvassa.</span><span class="sxs-lookup"><span data-stu-id="97cb9-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="97cb9-115">3. példa: az előfizetésben szereplő összes tároló-nyilvántartó-bejegyzés beszerzése</span><span class="sxs-lookup"><span data-stu-id="97cb9-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="97cb9-116">Ez a parancs beilleszti az előfizetéshez tartozó összes tároló-nyilvántartót.</span><span class="sxs-lookup"><span data-stu-id="97cb9-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="97cb9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97cb9-117">PARAMETERS</span></span>

### <span data-ttu-id="97cb9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97cb9-118">-DefaultProfile</span></span>
<span data-ttu-id="97cb9-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97cb9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97cb9-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="97cb9-120">-IncludeDetail</span></span>
<span data-ttu-id="97cb9-121">További részletek megjelenítése a tároló beállításjegyzékéről.</span><span class="sxs-lookup"><span data-stu-id="97cb9-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="97cb9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97cb9-122">-Name</span></span>
<span data-ttu-id="97cb9-123">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="97cb9-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="97cb9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97cb9-124">-ResourceGroupName</span></span>
<span data-ttu-id="97cb9-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="97cb9-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="97cb9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97cb9-126">-ResourceId</span></span>
<span data-ttu-id="97cb9-127">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="97cb9-127">The container registry resource id</span></span>

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

### <span data-ttu-id="97cb9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97cb9-128">CommonParameters</span></span>
<span data-ttu-id="97cb9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97cb9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97cb9-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="97cb9-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97cb9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97cb9-131">INPUTS</span></span>

### <span data-ttu-id="97cb9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="97cb9-132">System.String</span></span>

## <span data-ttu-id="97cb9-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97cb9-133">OUTPUTS</span></span>

### <span data-ttu-id="97cb9-134">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97cb9-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="97cb9-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97cb9-135">NOTES</span></span>

## <span data-ttu-id="97cb9-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97cb9-136">RELATED LINKS</span></span>

[<span data-ttu-id="97cb9-137">Új – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97cb9-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="97cb9-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97cb9-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="97cb9-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97cb9-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

