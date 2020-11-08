---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186629"
---
# <span data-ttu-id="af9a8-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="af9a8-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="af9a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af9a8-102">SYNOPSIS</span></span>
<span data-ttu-id="af9a8-103">Beilleszti egy eszköz konfigurált felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="af9a8-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="af9a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af9a8-104">SYNTAX</span></span>

### <span data-ttu-id="af9a8-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af9a8-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9a8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9a8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9a8-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9a8-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9a8-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9a8-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="af9a8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="af9a8-109">DESCRIPTION</span></span>
<span data-ttu-id="af9a8-110">A **Get-AzStackEdgeUser** parancsmag felsorolja azokat a felhasználókat, akik egy halom Edge-eszközhöz vannak konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="af9a8-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="af9a8-111">Ha egy adott felhasználóról szeretne részleteket bemutatni, a paraméterekben Megemlítheti a nevet.</span><span class="sxs-lookup"><span data-stu-id="af9a8-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="af9a8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="af9a8-112">EXAMPLES</span></span>

### <span data-ttu-id="af9a8-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="af9a8-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="af9a8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af9a8-114">PARAMETERS</span></span>

### <span data-ttu-id="af9a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9a8-115">-DefaultProfile</span></span>
<span data-ttu-id="af9a8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af9a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9a8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="af9a8-117">-DeviceName</span></span>
<span data-ttu-id="af9a8-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="af9a8-118">Device Name</span></span>

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

### <span data-ttu-id="af9a8-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="af9a8-119">-DeviceObject</span></span>
<span data-ttu-id="af9a8-120">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="af9a8-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="af9a8-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af9a8-121">-Name</span></span>
<span data-ttu-id="af9a8-122">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="af9a8-122">Username</span></span>

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

### <span data-ttu-id="af9a8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9a8-123">-ResourceGroupName</span></span>
<span data-ttu-id="af9a8-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="af9a8-124">Resource Group Name</span></span>

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

### <span data-ttu-id="af9a8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af9a8-125">-ResourceId</span></span>
<span data-ttu-id="af9a8-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="af9a8-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="af9a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9a8-127">CommonParameters</span></span>
<span data-ttu-id="af9a8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af9a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9a8-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="af9a8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9a8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af9a8-130">INPUTS</span></span>

### <span data-ttu-id="af9a8-131">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="af9a8-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="af9a8-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af9a8-132">OUTPUTS</span></span>

### <span data-ttu-id="af9a8-133">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="af9a8-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="af9a8-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af9a8-134">NOTES</span></span>

## <span data-ttu-id="af9a8-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af9a8-135">RELATED LINKS</span></span>