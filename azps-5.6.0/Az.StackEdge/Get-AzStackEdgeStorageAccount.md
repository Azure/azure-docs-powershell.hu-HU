---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: a5844e4d03be96d4835a7bf83b2128958cee0b5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939857"
---
# <span data-ttu-id="e0ba7-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0ba7-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="e0ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ba7-103">Beveszi a Edge Storage-fiókokat az eszközön.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="e0ba7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0ba7-104">SYNTAX</span></span>

### <span data-ttu-id="e0ba7-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0ba7-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0ba7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ba7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0ba7-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ba7-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0ba7-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ba7-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e0ba7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0ba7-109">DESCRIPTION</span></span>
<span data-ttu-id="e0ba7-110">A **Get-AzStackEdgeStorageAccount** parancsmag a Stack Edge-eszközön elérhetőVé válik a Edge Storage-fiókok számára.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="e0ba7-111">A Név paraméterként megadhatja a parancsmagban egy adott Edge Storage-fiók adatait.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="e0ba7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0ba7-112">EXAMPLES</span></span>

### <span data-ttu-id="e0ba7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e0ba7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="e0ba7-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e0ba7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="e0ba7-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="e0ba7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="e0ba7-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="e0ba7-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="e0ba7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0ba7-117">PARAMETERS</span></span>

### <span data-ttu-id="e0ba7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ba7-118">-DefaultProfile</span></span>
<span data-ttu-id="e0ba7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0ba7-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e0ba7-120">-DeviceName</span></span>
<span data-ttu-id="e0ba7-121">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="e0ba7-121">Device Name</span></span>

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

### <span data-ttu-id="e0ba7-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e0ba7-122">-DeviceObject</span></span>
<span data-ttu-id="e0ba7-123">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="e0ba7-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e0ba7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e0ba7-124">-Name</span></span>
<span data-ttu-id="e0ba7-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="e0ba7-125">Resource Name</span></span>

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

### <span data-ttu-id="e0ba7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ba7-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0ba7-127">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e0ba7-127">Resource Group Name</span></span>

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

### <span data-ttu-id="e0ba7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ba7-128">-ResourceId</span></span>
<span data-ttu-id="e0ba7-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ba7-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="e0ba7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ba7-130">CommonParameters</span></span>
<span data-ttu-id="e0ba7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ba7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0ba7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ba7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0ba7-133">INPUTS</span></span>

### <span data-ttu-id="e0ba7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e0ba7-134">System.String</span></span>

### <span data-ttu-id="e0ba7-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e0ba7-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="e0ba7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0ba7-136">OUTPUTS</span></span>

### <span data-ttu-id="e0ba7-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0ba7-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="e0ba7-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0ba7-138">NOTES</span></span>

## <span data-ttu-id="e0ba7-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0ba7-139">RELATED LINKS</span></span>
