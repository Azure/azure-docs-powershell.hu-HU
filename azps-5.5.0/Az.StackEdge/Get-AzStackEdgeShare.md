---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156138"
---
# <span data-ttu-id="53c15-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="53c15-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="53c15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53c15-102">SYNOPSIS</span></span>
<span data-ttu-id="53c15-103">Az eszközhöz elérhető megosztások lekérhetők.</span><span class="sxs-lookup"><span data-stu-id="53c15-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="53c15-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53c15-104">SYNTAX</span></span>

### <span data-ttu-id="53c15-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53c15-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53c15-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53c15-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53c15-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53c15-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53c15-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53c15-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="53c15-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53c15-109">DESCRIPTION</span></span>
<span data-ttu-id="53c15-110">A **Get-AzStackEdgeShare** parancsmag megkapja az elérhető megosztásokat egy Stack Edge-es eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="53c15-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="53c15-111">Ha a Név meg van biztosítanak, akkor a megosztás név szerint történik.</span><span class="sxs-lookup"><span data-stu-id="53c15-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="53c15-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53c15-112">EXAMPLES</span></span>

### <span data-ttu-id="53c15-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="53c15-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="53c15-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53c15-114">PARAMETERS</span></span>

### <span data-ttu-id="53c15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c15-115">-DefaultProfile</span></span>
<span data-ttu-id="53c15-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53c15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53c15-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="53c15-117">-DeviceName</span></span>
<span data-ttu-id="53c15-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="53c15-118">Device Name</span></span>

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

### <span data-ttu-id="53c15-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="53c15-119">-DeviceObject</span></span>
<span data-ttu-id="53c15-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="53c15-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="53c15-121">-Name</span><span class="sxs-lookup"><span data-stu-id="53c15-121">-Name</span></span>
<span data-ttu-id="53c15-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="53c15-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53c15-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c15-123">-ResourceGroupName</span></span>
<span data-ttu-id="53c15-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="53c15-124">Resource Group Name</span></span>

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

### <span data-ttu-id="53c15-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53c15-125">-ResourceId</span></span>
<span data-ttu-id="53c15-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="53c15-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="53c15-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c15-127">CommonParameters</span></span>
<span data-ttu-id="53c15-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c15-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c15-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53c15-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c15-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53c15-130">INPUTS</span></span>

### <span data-ttu-id="53c15-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="53c15-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="53c15-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53c15-132">OUTPUTS</span></span>

### <span data-ttu-id="53c15-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="53c15-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="53c15-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53c15-134">NOTES</span></span>

## <span data-ttu-id="53c15-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53c15-135">RELATED LINKS</span></span>
