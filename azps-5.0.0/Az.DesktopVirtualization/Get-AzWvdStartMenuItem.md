---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: d4390f7de7b9fb91cf998050f192a3ba282e9585
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297065"
---
# <span data-ttu-id="4f395-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="4f395-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="4f395-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f395-102">SYNOPSIS</span></span>
<span data-ttu-id="4f395-103">A Start menü elemeinek listája az adott alkalmazás csoportban</span><span class="sxs-lookup"><span data-stu-id="4f395-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="4f395-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f395-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4f395-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f395-105">DESCRIPTION</span></span>
<span data-ttu-id="4f395-106">A Start menü elemeinek listája az adott alkalmazás csoportban</span><span class="sxs-lookup"><span data-stu-id="4f395-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="4f395-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4f395-107">EXAMPLES</span></span>

### <span data-ttu-id="4f395-108">2. példa: a Windows Virtual Desktop Start menü elemeinek listája</span><span class="sxs-lookup"><span data-stu-id="4f395-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="4f395-109">Ez a parancs felsorolja a Windows Virtual Desktop Start menü elemeit egy alkalmazás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="4f395-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="4f395-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f395-110">PARAMETERS</span></span>

### <span data-ttu-id="4f395-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="4f395-111">-ApplicationGroupName</span></span>
<span data-ttu-id="4f395-112">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="4f395-112">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f395-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f395-113">-DefaultProfile</span></span>
<span data-ttu-id="4f395-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f395-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f395-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f395-115">-ResourceGroupName</span></span>
<span data-ttu-id="4f395-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4f395-116">The name of the resource group.</span></span>
<span data-ttu-id="4f395-117">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="4f395-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f395-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f395-118">-SubscriptionId</span></span>
<span data-ttu-id="4f395-119">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4f395-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f395-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f395-120">CommonParameters</span></span>
<span data-ttu-id="4f395-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f395-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f395-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4f395-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f395-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f395-123">INPUTS</span></span>

## <span data-ttu-id="4f395-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f395-124">OUTPUTS</span></span>

### <span data-ttu-id="4f395-125">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="4f395-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IStartMenuItem</span></span>

## <span data-ttu-id="4f395-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f395-126">NOTES</span></span>

<span data-ttu-id="4f395-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4f395-127">ALIASES</span></span>

## <span data-ttu-id="4f395-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f395-128">RELATED LINKS</span></span>

