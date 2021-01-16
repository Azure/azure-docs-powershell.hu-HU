---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362779"
---
# <span data-ttu-id="78860-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="78860-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="78860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78860-102">SYNOPSIS</span></span>
<span data-ttu-id="78860-103">Az eseményindítók beállítása egy eszközön</span><span class="sxs-lookup"><span data-stu-id="78860-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="78860-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="78860-104">SYNTAX</span></span>

### <span data-ttu-id="78860-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78860-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78860-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78860-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78860-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78860-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78860-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78860-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="78860-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="78860-109">DESCRIPTION</span></span>
<span data-ttu-id="78860-110">A **Get-AzDataBoxEdgeTriger** parancsmag kapja meg az eszköz eseményindítóit.</span><span class="sxs-lookup"><span data-stu-id="78860-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="78860-111">A nevet paraméterként megadhatja a parancsmagban egy adott eseményindító részleteinek lehívásakor.</span><span class="sxs-lookup"><span data-stu-id="78860-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="78860-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="78860-112">EXAMPLES</span></span>

### <span data-ttu-id="78860-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="78860-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="78860-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78860-114">PARAMETERS</span></span>

### <span data-ttu-id="78860-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78860-115">-DefaultProfile</span></span>
<span data-ttu-id="78860-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78860-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78860-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="78860-117">-DeviceName</span></span>
<span data-ttu-id="78860-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="78860-118">Device Name</span></span>

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

### <span data-ttu-id="78860-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="78860-119">-DeviceObject</span></span>
<span data-ttu-id="78860-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="78860-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="78860-121">-Name</span><span class="sxs-lookup"><span data-stu-id="78860-121">-Name</span></span>
<span data-ttu-id="78860-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="78860-122">Resource Name</span></span>

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

### <span data-ttu-id="78860-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78860-123">-ResourceGroupName</span></span>
<span data-ttu-id="78860-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="78860-124">Resource Group Name</span></span>

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

### <span data-ttu-id="78860-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78860-125">-ResourceId</span></span>
<span data-ttu-id="78860-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="78860-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="78860-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78860-127">CommonParameters</span></span>
<span data-ttu-id="78860-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78860-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78860-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78860-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78860-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78860-130">INPUTS</span></span>

### <span data-ttu-id="78860-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="78860-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="78860-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78860-132">OUTPUTS</span></span>

### <span data-ttu-id="78860-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="78860-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="78860-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="78860-134">NOTES</span></span>

## <span data-ttu-id="78860-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78860-135">RELATED LINKS</span></span>
