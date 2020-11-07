---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 174f6c58dfeb2d79a19b08cc1f360ea05e0c4736
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844121"
---
# <span data-ttu-id="b4304-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b4304-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="b4304-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4304-102">SYNOPSIS</span></span>
<span data-ttu-id="b4304-103">Egy eszközön az Edge Storage-fiók tárolóját kapja.</span><span class="sxs-lookup"><span data-stu-id="b4304-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="b4304-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4304-104">SYNTAX</span></span>

### <span data-ttu-id="b4304-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4304-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4304-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4304-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4304-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4304-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4304-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4304-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="b4304-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4304-109">DESCRIPTION</span></span>
<span data-ttu-id="b4304-110">A **Get-AzDataBoxEdgeStorageContainer** parancsmag egy adatmező szélén lévő eszközön megkapja az Edge Storage-fiók tároló tárolóját.</span><span class="sxs-lookup"><span data-stu-id="b4304-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="b4304-111">Megadhatja, hogy egy adott tárolóhoz tartozó adatok beolvasásakor a parancsmag paraméterként adja meg a nevet.</span><span class="sxs-lookup"><span data-stu-id="b4304-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="b4304-112">Példák</span><span class="sxs-lookup"><span data-stu-id="b4304-112">EXAMPLES</span></span>

### <span data-ttu-id="b4304-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4304-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="b4304-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="b4304-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="b4304-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="b4304-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="b4304-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4304-116">PARAMETERS</span></span>

### <span data-ttu-id="b4304-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4304-117">-DefaultProfile</span></span>
<span data-ttu-id="b4304-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4304-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4304-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b4304-119">-DeviceName</span></span>
<span data-ttu-id="b4304-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="b4304-120">Device Name</span></span>

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

### <span data-ttu-id="b4304-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4304-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="b4304-122">Létező EdgeStorageAccount-név megadása</span><span class="sxs-lookup"><span data-stu-id="b4304-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="b4304-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="b4304-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="b4304-124">Meglévő EdgeStorageAccount-objektum nyújtása</span><span class="sxs-lookup"><span data-stu-id="b4304-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="b4304-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4304-125">-Name</span></span>
<span data-ttu-id="b4304-126">A EdgeStorageContainer neve</span><span class="sxs-lookup"><span data-stu-id="b4304-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="b4304-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4304-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4304-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b4304-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b4304-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4304-129">-ResourceId</span></span>
<span data-ttu-id="b4304-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4304-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="b4304-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4304-131">CommonParameters</span></span>
<span data-ttu-id="b4304-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4304-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4304-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4304-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4304-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4304-134">INPUTS</span></span>

### <span data-ttu-id="b4304-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b4304-135">System.String</span></span>

### <span data-ttu-id="b4304-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4304-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="b4304-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4304-137">OUTPUTS</span></span>

### <span data-ttu-id="b4304-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b4304-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="b4304-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4304-139">NOTES</span></span>

## <span data-ttu-id="b4304-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4304-140">RELATED LINKS</span></span>
