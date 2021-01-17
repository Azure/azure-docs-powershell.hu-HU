---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367931"
---
# <span data-ttu-id="463df-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="463df-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="463df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="463df-102">SYNOPSIS</span></span>
<span data-ttu-id="463df-103">Lekérte az eszközön a tárfiókhoz tartozó hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="463df-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="463df-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="463df-104">SYNTAX</span></span>

### <span data-ttu-id="463df-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="463df-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="463df-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="463df-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="463df-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="463df-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="463df-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="463df-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="463df-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="463df-109">DESCRIPTION</span></span>
<span data-ttu-id="463df-110">A **Get-AzStackEdgeStorageAccountCredential** parancsmag a Stack Edge eszközön a megfelelő tárfiók hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="463df-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="463df-111">A Tárfiók adott hitelesítő adatairól a Név, az Erőforráscsoport neve és az Eszköznév paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="463df-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="463df-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="463df-112">EXAMPLES</span></span>

### <span data-ttu-id="463df-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="463df-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="463df-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="463df-114">PARAMETERS</span></span>

### <span data-ttu-id="463df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463df-115">-DefaultProfile</span></span>
<span data-ttu-id="463df-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="463df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="463df-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="463df-117">-DeviceName</span></span>
<span data-ttu-id="463df-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="463df-118">Device Name</span></span>

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

### <span data-ttu-id="463df-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="463df-119">-DeviceObject</span></span>
<span data-ttu-id="463df-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="463df-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="463df-121">-Name</span><span class="sxs-lookup"><span data-stu-id="463df-121">-Name</span></span>
<span data-ttu-id="463df-122">A használni használt tárfiók neve</span><span class="sxs-lookup"><span data-stu-id="463df-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="463df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="463df-123">-ResourceGroupName</span></span>
<span data-ttu-id="463df-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="463df-124">Resource Group Name</span></span>

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

### <span data-ttu-id="463df-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="463df-125">-ResourceId</span></span>
<span data-ttu-id="463df-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="463df-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="463df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463df-127">CommonParameters</span></span>
<span data-ttu-id="463df-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463df-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="463df-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463df-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="463df-130">INPUTS</span></span>

### <span data-ttu-id="463df-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="463df-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="463df-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="463df-132">OUTPUTS</span></span>

### <span data-ttu-id="463df-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="463df-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="463df-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="463df-134">NOTES</span></span>

## <span data-ttu-id="463df-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="463df-135">RELATED LINKS</span></span>
