---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025934"
---
# <span data-ttu-id="a4ad1-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a4ad1-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="a4ad1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ad1-103">Egy eszközön az Edge Storage-fiók tárolóját kapja.</span><span class="sxs-lookup"><span data-stu-id="a4ad1-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="a4ad1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4ad1-104">SYNTAX</span></span>

### <span data-ttu-id="a4ad1-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4ad1-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ad1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ad1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4ad1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ad1-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4ad1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ad1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="a4ad1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4ad1-109">DESCRIPTION</span></span>
<span data-ttu-id="a4ad1-110">A **Get-AzStackEdgeStorageContainer** parancsmag az Edge tárterületét tartalmazó eszközön kapja meg a tároló tárolót.</span><span class="sxs-lookup"><span data-stu-id="a4ad1-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="a4ad1-111">Megadhatja, hogy egy adott tárolóhoz tartozó adatok beolvasásakor a parancsmag paraméterként adja meg a nevet.</span><span class="sxs-lookup"><span data-stu-id="a4ad1-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="a4ad1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a4ad1-112">EXAMPLES</span></span>

### <span data-ttu-id="a4ad1-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a4ad1-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="a4ad1-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a4ad1-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="a4ad1-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a4ad1-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="a4ad1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4ad1-116">PARAMETERS</span></span>

### <span data-ttu-id="a4ad1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ad1-117">-DefaultProfile</span></span>
<span data-ttu-id="a4ad1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4ad1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ad1-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a4ad1-119">-DeviceName</span></span>
<span data-ttu-id="a4ad1-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="a4ad1-120">Device Name</span></span>

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

### <span data-ttu-id="a4ad1-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a4ad1-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="a4ad1-122">Létező EdgeStorageAccount-név megadása</span><span class="sxs-lookup"><span data-stu-id="a4ad1-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="a4ad1-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="a4ad1-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="a4ad1-124">Meglévő EdgeStorageAccount-objektum nyújtása</span><span class="sxs-lookup"><span data-stu-id="a4ad1-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="a4ad1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4ad1-125">-Name</span></span>
<span data-ttu-id="a4ad1-126">A EdgeStorageContainer neve</span><span class="sxs-lookup"><span data-stu-id="a4ad1-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="a4ad1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ad1-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4ad1-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a4ad1-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a4ad1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4ad1-129">-ResourceId</span></span>
<span data-ttu-id="a4ad1-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4ad1-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="a4ad1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ad1-131">CommonParameters</span></span>
<span data-ttu-id="a4ad1-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4ad1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ad1-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4ad1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ad1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4ad1-134">INPUTS</span></span>

### <span data-ttu-id="a4ad1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ad1-135">System.String</span></span>

### <span data-ttu-id="a4ad1-136">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a4ad1-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="a4ad1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4ad1-137">OUTPUTS</span></span>

### <span data-ttu-id="a4ad1-138">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a4ad1-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="a4ad1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4ad1-139">NOTES</span></span>

## <span data-ttu-id="a4ad1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4ad1-140">RELATED LINKS</span></span>
