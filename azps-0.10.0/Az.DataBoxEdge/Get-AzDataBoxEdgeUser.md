---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: 0ab290934a956282a16d9e2321b2c5ed948f33af
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844117"
---
# <span data-ttu-id="d65d0-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="d65d0-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="d65d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d65d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d65d0-103">Beilleszti egy eszköz konfigurált felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="d65d0-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="d65d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d65d0-104">SYNTAX</span></span>

### <span data-ttu-id="d65d0-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d65d0-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d65d0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d65d0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d65d0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d65d0-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d65d0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d65d0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="d65d0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d65d0-109">DESCRIPTION</span></span>
<span data-ttu-id="d65d0-110">A **Get-AzDataBoxEdgeUser** parancsmag felsorolja azokat a felhasználókat, akiknek konfigurálva van az adatmező szélén lévő eszköz.</span><span class="sxs-lookup"><span data-stu-id="d65d0-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="d65d0-111">Ha egy adott felhasználóról szeretne részleteket bemutatni, a paraméterekben Megemlítheti a nevet.</span><span class="sxs-lookup"><span data-stu-id="d65d0-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="d65d0-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d65d0-112">EXAMPLES</span></span>

### <span data-ttu-id="d65d0-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d65d0-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="d65d0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d65d0-114">PARAMETERS</span></span>

### <span data-ttu-id="d65d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65d0-115">-DefaultProfile</span></span>
<span data-ttu-id="d65d0-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d65d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d65d0-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d65d0-117">-DeviceName</span></span>
<span data-ttu-id="d65d0-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="d65d0-118">Device Name</span></span>

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

### <span data-ttu-id="d65d0-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d65d0-119">-DeviceObject</span></span>
<span data-ttu-id="d65d0-120">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="d65d0-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="d65d0-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d65d0-121">-Name</span></span>
<span data-ttu-id="d65d0-122">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="d65d0-122">Username</span></span>

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

### <span data-ttu-id="d65d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="d65d0-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d65d0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d65d0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d65d0-125">-ResourceId</span></span>
<span data-ttu-id="d65d0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d65d0-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="d65d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65d0-127">CommonParameters</span></span>
<span data-ttu-id="d65d0-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d65d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65d0-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d65d0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65d0-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d65d0-130">INPUTS</span></span>

### <span data-ttu-id="d65d0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d65d0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="d65d0-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d65d0-132">OUTPUTS</span></span>

### <span data-ttu-id="d65d0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="d65d0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="d65d0-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d65d0-134">NOTES</span></span>

## <span data-ttu-id="d65d0-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d65d0-135">RELATED LINKS</span></span>
