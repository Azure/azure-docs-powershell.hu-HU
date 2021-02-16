---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3f7ebc42efc2ad5ba73079fd2774614b941f432b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167834"
---
# <span data-ttu-id="91e40-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="91e40-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="91e40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e40-102">SYNOPSIS</span></span>
<span data-ttu-id="91e40-103">Egy Edge Storage-fiók tárolóit kapja meg egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="91e40-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="91e40-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91e40-104">SYNTAX</span></span>

### <span data-ttu-id="91e40-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91e40-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91e40-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91e40-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91e40-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="91e40-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91e40-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91e40-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="91e40-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91e40-109">DESCRIPTION</span></span>
<span data-ttu-id="91e40-110">A **Get-AzDataBoxEdgeStorageContainer** parancsmag egy Data Box Edge-eszközön található Edge Storage-fiók tárolóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91e40-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="91e40-111">A nevet paraméterként megadhatja a parancsmagban egy adott tároló részleteinek lehívása érdekében.</span><span class="sxs-lookup"><span data-stu-id="91e40-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="91e40-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91e40-112">EXAMPLES</span></span>

### <span data-ttu-id="91e40-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="91e40-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="91e40-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="91e40-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="91e40-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="91e40-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="91e40-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91e40-116">PARAMETERS</span></span>

### <span data-ttu-id="91e40-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e40-117">-DefaultProfile</span></span>
<span data-ttu-id="91e40-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91e40-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91e40-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="91e40-119">-DeviceName</span></span>
<span data-ttu-id="91e40-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="91e40-120">Device Name</span></span>

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

### <span data-ttu-id="91e40-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="91e40-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="91e40-122">Meglévő EdgeStorageAccount nevének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="91e40-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="91e40-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="91e40-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="91e40-124">Meglévő EdgeStorageAccount objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="91e40-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91e40-125">-Name</span><span class="sxs-lookup"><span data-stu-id="91e40-125">-Name</span></span>
<span data-ttu-id="91e40-126">A EdgeStorageContainer neve</span><span class="sxs-lookup"><span data-stu-id="91e40-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="91e40-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e40-127">-ResourceGroupName</span></span>
<span data-ttu-id="91e40-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="91e40-128">Resource Group Name</span></span>

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

### <span data-ttu-id="91e40-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91e40-129">-ResourceId</span></span>
<span data-ttu-id="91e40-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="91e40-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="91e40-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e40-131">CommonParameters</span></span>
<span data-ttu-id="91e40-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e40-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e40-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91e40-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e40-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91e40-134">INPUTS</span></span>

### <span data-ttu-id="91e40-135">System.String</span><span class="sxs-lookup"><span data-stu-id="91e40-135">System.String</span></span>

### <span data-ttu-id="91e40-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91e40-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="91e40-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91e40-137">OUTPUTS</span></span>

### <span data-ttu-id="91e40-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="91e40-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="91e40-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91e40-139">NOTES</span></span>

## <span data-ttu-id="91e40-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91e40-140">RELATED LINKS</span></span>
