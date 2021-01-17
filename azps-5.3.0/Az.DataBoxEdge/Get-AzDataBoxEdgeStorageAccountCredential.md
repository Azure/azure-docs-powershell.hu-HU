---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477262"
---
# <span data-ttu-id="79696-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="79696-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="79696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79696-102">SYNOPSIS</span></span>
<span data-ttu-id="79696-103">Lekérte az eszközön a tárfiókhoz tartozó hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="79696-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="79696-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79696-104">SYNTAX</span></span>

### <span data-ttu-id="79696-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79696-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79696-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79696-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79696-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79696-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79696-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79696-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="79696-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79696-109">DESCRIPTION</span></span>
<span data-ttu-id="79696-110">A **Get-AzDataBoxEdgeStorageAccountCredential** parancsmag megkapja a megfelelő tárfiók hitelesítő adatait a Data Box Edge eszközön.</span><span class="sxs-lookup"><span data-stu-id="79696-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="79696-111">A Tárfiók adott hitelesítő adatairól a Név, az Erőforráscsoport neve és az Eszköznév paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="79696-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="79696-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79696-112">EXAMPLES</span></span>

### <span data-ttu-id="79696-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="79696-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="79696-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79696-114">PARAMETERS</span></span>

### <span data-ttu-id="79696-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79696-115">-DefaultProfile</span></span>
<span data-ttu-id="79696-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79696-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79696-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="79696-117">-DeviceName</span></span>
<span data-ttu-id="79696-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="79696-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79696-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="79696-119">-DeviceObject</span></span>
<span data-ttu-id="79696-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="79696-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="79696-121">-Name</span><span class="sxs-lookup"><span data-stu-id="79696-121">-Name</span></span>
<span data-ttu-id="79696-122">A használni használt tárfiók neve</span><span class="sxs-lookup"><span data-stu-id="79696-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79696-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79696-123">-ResourceGroupName</span></span>
<span data-ttu-id="79696-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="79696-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79696-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79696-125">-ResourceId</span></span>
<span data-ttu-id="79696-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="79696-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79696-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79696-127">CommonParameters</span></span>
<span data-ttu-id="79696-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79696-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79696-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79696-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79696-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79696-130">INPUTS</span></span>

### <span data-ttu-id="79696-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="79696-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="79696-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79696-132">OUTPUTS</span></span>

### <span data-ttu-id="79696-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="79696-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="79696-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79696-134">NOTES</span></span>

## <span data-ttu-id="79696-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79696-135">RELATED LINKS</span></span>
