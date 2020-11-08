---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185170"
---
# <span data-ttu-id="39595-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39595-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="39595-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39595-102">SYNOPSIS</span></span>
<span data-ttu-id="39595-103">Megkapja az eszközön az Edge Storage fiókokat.</span><span class="sxs-lookup"><span data-stu-id="39595-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="39595-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39595-104">SYNTAX</span></span>

### <span data-ttu-id="39595-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39595-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39595-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39595-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39595-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="39595-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39595-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39595-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="39595-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="39595-109">DESCRIPTION</span></span>
<span data-ttu-id="39595-110">A **Get-AzStackEdgeStorageAccount** parancsmag a halom szélén elérhető eszközön elérhető peremhálózat-tároló fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="39595-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="39595-111">Megadhatja, hogy milyen név legyen a parancsmagban, hogy egy adott Edge tárterület-fiók adatai legyenek láthatók.</span><span class="sxs-lookup"><span data-stu-id="39595-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="39595-112">Példák</span><span class="sxs-lookup"><span data-stu-id="39595-112">EXAMPLES</span></span>

### <span data-ttu-id="39595-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="39595-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="39595-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="39595-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="39595-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="39595-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="39595-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="39595-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="39595-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39595-117">PARAMETERS</span></span>

### <span data-ttu-id="39595-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39595-118">-DefaultProfile</span></span>
<span data-ttu-id="39595-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39595-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39595-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="39595-120">-DeviceName</span></span>
<span data-ttu-id="39595-121">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="39595-121">Device Name</span></span>

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

### <span data-ttu-id="39595-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="39595-122">-DeviceObject</span></span>
<span data-ttu-id="39595-123">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="39595-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39595-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39595-124">-Name</span></span>
<span data-ttu-id="39595-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="39595-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39595-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39595-126">-ResourceGroupName</span></span>
<span data-ttu-id="39595-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="39595-127">Resource Group Name</span></span>

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

### <span data-ttu-id="39595-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39595-128">-ResourceId</span></span>
<span data-ttu-id="39595-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="39595-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39595-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39595-130">CommonParameters</span></span>
<span data-ttu-id="39595-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39595-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39595-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="39595-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39595-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39595-133">INPUTS</span></span>

### <span data-ttu-id="39595-134">System. String</span><span class="sxs-lookup"><span data-stu-id="39595-134">System.String</span></span>

### <span data-ttu-id="39595-135">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="39595-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="39595-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39595-136">OUTPUTS</span></span>

### <span data-ttu-id="39595-137">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39595-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="39595-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39595-138">NOTES</span></span>

## <span data-ttu-id="39595-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39595-139">RELATED LINKS</span></span>