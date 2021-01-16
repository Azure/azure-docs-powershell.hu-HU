---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333822"
---
# <span data-ttu-id="3b360-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3b360-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="3b360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b360-102">SYNOPSIS</span></span>
<span data-ttu-id="3b360-103">Beállítja az eszköz konfigurált felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="3b360-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="3b360-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3b360-104">SYNTAX</span></span>

### <span data-ttu-id="3b360-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b360-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b360-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b360-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b360-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b360-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b360-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b360-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="3b360-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3b360-109">DESCRIPTION</span></span>
<span data-ttu-id="3b360-110">A **Get-AzStackEdgeUser** parancsmag felsorolja a Stack Edge-es eszközhöz konfigurált felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="3b360-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="3b360-111">Megemlítheti a nevet a paraméterekben, ha egy adott felhasználó adatait meg kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="3b360-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="3b360-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3b360-112">EXAMPLES</span></span>

### <span data-ttu-id="3b360-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="3b360-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="3b360-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b360-114">PARAMETERS</span></span>

### <span data-ttu-id="3b360-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b360-115">-DefaultProfile</span></span>
<span data-ttu-id="3b360-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b360-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b360-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3b360-117">-DeviceName</span></span>
<span data-ttu-id="3b360-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="3b360-118">Device Name</span></span>

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

### <span data-ttu-id="3b360-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="3b360-119">-DeviceObject</span></span>
<span data-ttu-id="3b360-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="3b360-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="3b360-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3b360-121">-Name</span></span>
<span data-ttu-id="3b360-122">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="3b360-122">Username</span></span>

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

### <span data-ttu-id="3b360-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b360-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b360-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3b360-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3b360-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b360-125">-ResourceId</span></span>
<span data-ttu-id="3b360-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b360-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="3b360-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b360-127">CommonParameters</span></span>
<span data-ttu-id="3b360-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b360-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b360-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b360-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b360-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b360-130">INPUTS</span></span>

### <span data-ttu-id="3b360-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3b360-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="3b360-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b360-132">OUTPUTS</span></span>

### <span data-ttu-id="3b360-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3b360-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="3b360-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3b360-134">NOTES</span></span>

## <span data-ttu-id="3b360-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b360-135">RELATED LINKS</span></span>
