---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297068"
---
# <span data-ttu-id="c32cc-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c32cc-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="c32cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c32cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c32cc-103">A Windows virtuális asztali regisztrációs adatainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="c32cc-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c32cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c32cc-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c32cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c32cc-105">DESCRIPTION</span></span>
<span data-ttu-id="c32cc-106">A Windows virtuális asztali regisztrációs adatainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="c32cc-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c32cc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c32cc-107">EXAMPLES</span></span>

### <span data-ttu-id="c32cc-108">Példa 1: a Windows virtuális asztali regisztrációs token beszerzése</span><span class="sxs-lookup"><span data-stu-id="c32cc-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="c32cc-109">Ez a parancs egy Windows virtuális asztali regisztrációs tokent kap egy alkalmazáskészletben.</span><span class="sxs-lookup"><span data-stu-id="c32cc-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="c32cc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c32cc-110">PARAMETERS</span></span>

### <span data-ttu-id="c32cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32cc-111">-DefaultProfile</span></span>
<span data-ttu-id="c32cc-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c32cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c32cc-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c32cc-113">-HostPoolName</span></span>
<span data-ttu-id="c32cc-114">Állomáslista neve</span><span class="sxs-lookup"><span data-stu-id="c32cc-114">Host Pool Name</span></span>

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

### <span data-ttu-id="c32cc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c32cc-115">-ResourceGroupName</span></span>
<span data-ttu-id="c32cc-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c32cc-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c32cc-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c32cc-117">-SubscriptionId</span></span>
<span data-ttu-id="c32cc-118">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="c32cc-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32cc-119">CommonParameters</span></span>
<span data-ttu-id="c32cc-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c32cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32cc-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c32cc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32cc-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c32cc-122">INPUTS</span></span>

## <span data-ttu-id="c32cc-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c32cc-123">OUTPUTS</span></span>

### <span data-ttu-id="c32cc-124">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c32cc-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="c32cc-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c32cc-125">NOTES</span></span>

<span data-ttu-id="c32cc-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c32cc-126">ALIASES</span></span>

## <span data-ttu-id="c32cc-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c32cc-127">RELATED LINKS</span></span>

