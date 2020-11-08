---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013415"
---
# <span data-ttu-id="477cf-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="477cf-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="477cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="477cf-102">SYNOPSIS</span></span>
<span data-ttu-id="477cf-103">Megkapja az eszközön az Edge Storage fiókokat.</span><span class="sxs-lookup"><span data-stu-id="477cf-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="477cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="477cf-104">SYNTAX</span></span>

### <span data-ttu-id="477cf-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="477cf-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="477cf-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="477cf-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="477cf-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="477cf-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="477cf-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="477cf-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="477cf-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="477cf-109">DESCRIPTION</span></span>
<span data-ttu-id="477cf-110">A **Get-AzDataBoxEdgeStorageAccount** parancsmag az egy adatmező szélén lévő eszközön elérhető peremhálózat-tárolási fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="477cf-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="477cf-111">Megadhatja, hogy milyen név legyen a parancsmagban, hogy egy adott Edge tárterület-fiók adatai legyenek láthatók.</span><span class="sxs-lookup"><span data-stu-id="477cf-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="477cf-112">Példák</span><span class="sxs-lookup"><span data-stu-id="477cf-112">EXAMPLES</span></span>

### <span data-ttu-id="477cf-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="477cf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="477cf-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="477cf-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="477cf-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="477cf-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="477cf-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="477cf-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="477cf-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="477cf-117">PARAMETERS</span></span>

### <span data-ttu-id="477cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477cf-118">-DefaultProfile</span></span>
<span data-ttu-id="477cf-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="477cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="477cf-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="477cf-120">-DeviceName</span></span>
<span data-ttu-id="477cf-121">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="477cf-121">Device Name</span></span>

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

### <span data-ttu-id="477cf-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="477cf-122">-DeviceObject</span></span>
<span data-ttu-id="477cf-123">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="477cf-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="477cf-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="477cf-124">-Name</span></span>
<span data-ttu-id="477cf-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="477cf-125">Resource Name</span></span>

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

### <span data-ttu-id="477cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="477cf-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="477cf-127">Resource Group Name</span></span>

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

### <span data-ttu-id="477cf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="477cf-128">-ResourceId</span></span>
<span data-ttu-id="477cf-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="477cf-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="477cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477cf-130">CommonParameters</span></span>
<span data-ttu-id="477cf-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="477cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477cf-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="477cf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477cf-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="477cf-133">INPUTS</span></span>

### <span data-ttu-id="477cf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="477cf-134">System.String</span></span>

### <span data-ttu-id="477cf-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="477cf-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="477cf-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="477cf-136">OUTPUTS</span></span>

### <span data-ttu-id="477cf-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="477cf-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="477cf-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="477cf-138">NOTES</span></span>

## <span data-ttu-id="477cf-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="477cf-139">RELATED LINKS</span></span>
