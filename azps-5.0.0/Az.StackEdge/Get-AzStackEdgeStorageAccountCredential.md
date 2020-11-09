---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301742"
---
# <span data-ttu-id="5af7f-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5af7f-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="5af7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5af7f-102">SYNOPSIS</span></span>
<span data-ttu-id="5af7f-103">A tárolási fiók hitelesítő adatait kapja meg az eszközön.</span><span class="sxs-lookup"><span data-stu-id="5af7f-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="5af7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5af7f-104">SYNTAX</span></span>

### <span data-ttu-id="5af7f-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5af7f-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5af7f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5af7f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5af7f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5af7f-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5af7f-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5af7f-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5af7f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5af7f-109">DESCRIPTION</span></span>
<span data-ttu-id="5af7f-110">A **Get-AzStackEdgeStorageAccountCredential** parancsmag a megfelelő tárterület-fiók hitelesítő adatait a halom szélén lévő eszközön kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5af7f-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="5af7f-111">Megadhatja a név, az erőforráscsoport neve és az eszköz neve paramétert, amellyel információkat kaphat egy adott tárolási fiók hitelesítő adatairól.</span><span class="sxs-lookup"><span data-stu-id="5af7f-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="5af7f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="5af7f-112">EXAMPLES</span></span>

### <span data-ttu-id="5af7f-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5af7f-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="5af7f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5af7f-114">PARAMETERS</span></span>

### <span data-ttu-id="5af7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af7f-115">-DefaultProfile</span></span>
<span data-ttu-id="5af7f-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5af7f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5af7f-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5af7f-117">-DeviceName</span></span>
<span data-ttu-id="5af7f-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="5af7f-118">Device Name</span></span>

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

### <span data-ttu-id="5af7f-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5af7f-119">-DeviceObject</span></span>
<span data-ttu-id="5af7f-120">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="5af7f-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="5af7f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5af7f-121">-Name</span></span>
<span data-ttu-id="5af7f-122">A használandó tárterület-fiók neve</span><span class="sxs-lookup"><span data-stu-id="5af7f-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="5af7f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af7f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5af7f-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5af7f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5af7f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5af7f-125">-ResourceId</span></span>
<span data-ttu-id="5af7f-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5af7f-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="5af7f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af7f-127">CommonParameters</span></span>
<span data-ttu-id="5af7f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5af7f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af7f-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5af7f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af7f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5af7f-130">INPUTS</span></span>

### <span data-ttu-id="5af7f-131">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5af7f-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="5af7f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5af7f-132">OUTPUTS</span></span>

### <span data-ttu-id="5af7f-133">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5af7f-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="5af7f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5af7f-134">NOTES</span></span>

## <span data-ttu-id="5af7f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5af7f-135">RELATED LINKS</span></span>
