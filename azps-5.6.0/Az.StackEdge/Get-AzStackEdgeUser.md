---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 9d06873954e6a6880965781d2004d8b7b0c35bb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931434"
---
# <span data-ttu-id="41ad5-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="41ad5-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="41ad5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="41ad5-103">Beállítja az eszköz konfigurált felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="41ad5-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="41ad5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41ad5-104">SYNTAX</span></span>

### <span data-ttu-id="41ad5-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41ad5-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41ad5-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41ad5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41ad5-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="41ad5-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41ad5-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41ad5-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="41ad5-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41ad5-109">DESCRIPTION</span></span>
<span data-ttu-id="41ad5-110">A **Get-AzStackEdgeUser** parancsmag felsorolja a Stack Edge-es eszközhöz konfigurált felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="41ad5-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="41ad5-111">Megemlítheti a nevet a paraméterekben, ha egy adott felhasználó adatait meg kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="41ad5-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="41ad5-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41ad5-112">EXAMPLES</span></span>

### <span data-ttu-id="41ad5-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="41ad5-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="41ad5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41ad5-114">PARAMETERS</span></span>

### <span data-ttu-id="41ad5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ad5-115">-DefaultProfile</span></span>
<span data-ttu-id="41ad5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41ad5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41ad5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="41ad5-117">-DeviceName</span></span>
<span data-ttu-id="41ad5-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="41ad5-118">Device Name</span></span>

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

### <span data-ttu-id="41ad5-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="41ad5-119">-DeviceObject</span></span>
<span data-ttu-id="41ad5-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="41ad5-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="41ad5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="41ad5-121">-Name</span></span>
<span data-ttu-id="41ad5-122">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="41ad5-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41ad5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41ad5-123">-ResourceGroupName</span></span>
<span data-ttu-id="41ad5-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="41ad5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="41ad5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41ad5-125">-ResourceId</span></span>
<span data-ttu-id="41ad5-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="41ad5-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="41ad5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ad5-127">CommonParameters</span></span>
<span data-ttu-id="41ad5-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41ad5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ad5-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41ad5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ad5-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41ad5-130">INPUTS</span></span>

### <span data-ttu-id="41ad5-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="41ad5-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="41ad5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41ad5-132">OUTPUTS</span></span>

### <span data-ttu-id="41ad5-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="41ad5-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="41ad5-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41ad5-134">NOTES</span></span>

## <span data-ttu-id="41ad5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41ad5-135">RELATED LINKS</span></span>
