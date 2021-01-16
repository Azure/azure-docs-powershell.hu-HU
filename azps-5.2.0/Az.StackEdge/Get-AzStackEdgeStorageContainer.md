---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334553"
---
# <span data-ttu-id="daafa-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="daafa-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="daafa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daafa-102">SYNOPSIS</span></span>
<span data-ttu-id="daafa-103">Egy Edge Storage-fiók tárolóit kapja meg egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="daafa-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="daafa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="daafa-104">SYNTAX</span></span>

### <span data-ttu-id="daafa-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="daafa-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="daafa-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="daafa-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="daafa-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="daafa-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="daafa-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="daafa-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="daafa-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="daafa-109">DESCRIPTION</span></span>
<span data-ttu-id="daafa-110">A **Get-AzStackEdgeStorageContainer parancsmag** egy Stack Edge-eszközön található Edge Storage-fiók tárolóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="daafa-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="daafa-111">A nevet paraméterként megadhatja a parancsmagban egy adott tároló részleteinek lehívása érdekében.</span><span class="sxs-lookup"><span data-stu-id="daafa-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="daafa-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="daafa-112">EXAMPLES</span></span>

### <span data-ttu-id="daafa-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="daafa-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="daafa-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="daafa-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="daafa-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="daafa-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="daafa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="daafa-116">PARAMETERS</span></span>

### <span data-ttu-id="daafa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daafa-117">-DefaultProfile</span></span>
<span data-ttu-id="daafa-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="daafa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daafa-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="daafa-119">-DeviceName</span></span>
<span data-ttu-id="daafa-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="daafa-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daafa-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="daafa-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="daafa-122">Meglévő EdgeStorageAccount nevének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="daafa-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daafa-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="daafa-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="daafa-124">Meglévő EdgeStorageAccount objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="daafa-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daafa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="daafa-125">-Name</span></span>
<span data-ttu-id="daafa-126">A EdgeStorageContainer neve</span><span class="sxs-lookup"><span data-stu-id="daafa-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daafa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daafa-127">-ResourceGroupName</span></span>
<span data-ttu-id="daafa-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="daafa-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daafa-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daafa-129">-ResourceId</span></span>
<span data-ttu-id="daafa-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="daafa-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daafa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daafa-131">CommonParameters</span></span>
<span data-ttu-id="daafa-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daafa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daafa-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="daafa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daafa-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="daafa-134">INPUTS</span></span>

### <span data-ttu-id="daafa-135">System.String</span><span class="sxs-lookup"><span data-stu-id="daafa-135">System.String</span></span>

### <span data-ttu-id="daafa-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daafa-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="daafa-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="daafa-137">OUTPUTS</span></span>

### <span data-ttu-id="daafa-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="daafa-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="daafa-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="daafa-139">NOTES</span></span>

## <span data-ttu-id="daafa-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="daafa-140">RELATED LINKS</span></span>
