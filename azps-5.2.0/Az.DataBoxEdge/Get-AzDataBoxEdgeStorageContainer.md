---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3f7ebc42efc2ad5ba73079fd2774614b941f432b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331613"
---
# <span data-ttu-id="acc4d-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="acc4d-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="acc4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acc4d-102">SYNOPSIS</span></span>
<span data-ttu-id="acc4d-103">Egy Edge Storage-fiók tárolóit kapja meg egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="acc4d-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="acc4d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="acc4d-104">SYNTAX</span></span>

### <span data-ttu-id="acc4d-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="acc4d-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc4d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc4d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acc4d-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc4d-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acc4d-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc4d-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="acc4d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="acc4d-109">DESCRIPTION</span></span>
<span data-ttu-id="acc4d-110">A **Get-AzDataBoxEdgeStorageContainer** parancsmag egy Data Box Edge-eszközön található Edge Storage-fiók tárolóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="acc4d-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="acc4d-111">A nevet paraméterként megadhatja a parancsmagban egy adott tároló részleteinek lehívása érdekében.</span><span class="sxs-lookup"><span data-stu-id="acc4d-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="acc4d-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="acc4d-112">EXAMPLES</span></span>

### <span data-ttu-id="acc4d-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="acc4d-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="acc4d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="acc4d-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="acc4d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="acc4d-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="acc4d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acc4d-116">PARAMETERS</span></span>

### <span data-ttu-id="acc4d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc4d-117">-DefaultProfile</span></span>
<span data-ttu-id="acc4d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acc4d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc4d-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="acc4d-119">-DeviceName</span></span>
<span data-ttu-id="acc4d-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="acc4d-120">Device Name</span></span>

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

### <span data-ttu-id="acc4d-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="acc4d-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="acc4d-122">Meglévő EdgeStorageAccount nevének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="acc4d-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="acc4d-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="acc4d-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="acc4d-124">Meglévő EdgeStorageAccount objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc4d-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="acc4d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="acc4d-125">-Name</span></span>
<span data-ttu-id="acc4d-126">A EdgeStorageContainer neve</span><span class="sxs-lookup"><span data-stu-id="acc4d-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="acc4d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc4d-127">-ResourceGroupName</span></span>
<span data-ttu-id="acc4d-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="acc4d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="acc4d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acc4d-129">-ResourceId</span></span>
<span data-ttu-id="acc4d-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="acc4d-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="acc4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc4d-131">CommonParameters</span></span>
<span data-ttu-id="acc4d-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc4d-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acc4d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc4d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acc4d-134">INPUTS</span></span>

### <span data-ttu-id="acc4d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="acc4d-135">System.String</span></span>

### <span data-ttu-id="acc4d-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="acc4d-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="acc4d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acc4d-137">OUTPUTS</span></span>

### <span data-ttu-id="acc4d-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="acc4d-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="acc4d-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="acc4d-139">NOTES</span></span>

## <span data-ttu-id="acc4d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acc4d-140">RELATED LINKS</span></span>
