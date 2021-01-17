---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480480"
---
# <span data-ttu-id="3c9d6-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3c9d6-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="3c9d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9d6-103">Beállítja az eszköz konfigurált felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="3c9d6-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="3c9d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c9d6-104">SYNTAX</span></span>

### <span data-ttu-id="3c9d6-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c9d6-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c9d6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c9d6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c9d6-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c9d6-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c9d6-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c9d6-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="3c9d6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c9d6-109">DESCRIPTION</span></span>
<span data-ttu-id="3c9d6-110">A **Get-AzDataBoxEdgeUser** parancsmag felsorolja a Data Box Edge-es eszközhöz konfigurált felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="3c9d6-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="3c9d6-111">Megemlítheti a nevet a paraméterekben, ha egy adott felhasználó adatait meg kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="3c9d6-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="3c9d6-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c9d6-112">EXAMPLES</span></span>

### <span data-ttu-id="3c9d6-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="3c9d6-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="3c9d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c9d6-114">PARAMETERS</span></span>

### <span data-ttu-id="3c9d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9d6-115">-DefaultProfile</span></span>
<span data-ttu-id="3c9d6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c9d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c9d6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3c9d6-117">-DeviceName</span></span>
<span data-ttu-id="3c9d6-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="3c9d6-118">Device Name</span></span>

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

### <span data-ttu-id="3c9d6-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="3c9d6-119">-DeviceObject</span></span>
<span data-ttu-id="3c9d6-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="3c9d6-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="3c9d6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3c9d6-121">-Name</span></span>
<span data-ttu-id="3c9d6-122">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="3c9d6-122">Username</span></span>

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

### <span data-ttu-id="3c9d6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c9d6-123">-ResourceGroupName</span></span>
<span data-ttu-id="3c9d6-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3c9d6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3c9d6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c9d6-125">-ResourceId</span></span>
<span data-ttu-id="3c9d6-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c9d6-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="3c9d6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9d6-127">CommonParameters</span></span>
<span data-ttu-id="3c9d6-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c9d6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9d6-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c9d6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9d6-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c9d6-130">INPUTS</span></span>

### <span data-ttu-id="3c9d6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3c9d6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="3c9d6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c9d6-132">OUTPUTS</span></span>

### <span data-ttu-id="3c9d6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3c9d6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="3c9d6-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c9d6-134">NOTES</span></span>

## <span data-ttu-id="3c9d6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c9d6-135">RELATED LINKS</span></span>
