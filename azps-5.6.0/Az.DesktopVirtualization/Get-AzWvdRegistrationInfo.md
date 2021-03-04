---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 868cbf6aaaf9b9c304c6afa65e63e6eca12910d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923633"
---
# <span data-ttu-id="67238-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="67238-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="67238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67238-102">SYNOPSIS</span></span>
<span data-ttu-id="67238-103">Szerezze be a Windows virtuális asztali regisztrációs adatait.</span><span class="sxs-lookup"><span data-stu-id="67238-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="67238-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="67238-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="67238-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="67238-105">DESCRIPTION</span></span>
<span data-ttu-id="67238-106">Szerezze be a Windows virtuális asztali regisztrációs adatait.</span><span class="sxs-lookup"><span data-stu-id="67238-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="67238-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="67238-107">EXAMPLES</span></span>

### <span data-ttu-id="67238-108">1. példa: Windows virtuális asztali regisztrációs jogkivonat beszerzése</span><span class="sxs-lookup"><span data-stu-id="67238-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="67238-109">Ez a parancs egy Windows virtuális asztali regisztrációs jogkivonatot kap egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="67238-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="67238-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67238-110">PARAMETERS</span></span>

### <span data-ttu-id="67238-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67238-111">-DefaultProfile</span></span>
<span data-ttu-id="67238-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67238-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67238-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="67238-113">-HostPoolName</span></span>
<span data-ttu-id="67238-114">Állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="67238-114">Host Pool Name</span></span>

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

### <span data-ttu-id="67238-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67238-115">-ResourceGroupName</span></span>
<span data-ttu-id="67238-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="67238-116">Resource Group Name</span></span>

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

### <span data-ttu-id="67238-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67238-117">-SubscriptionId</span></span>
<span data-ttu-id="67238-118">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="67238-118">Subscription Id</span></span>

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

### <span data-ttu-id="67238-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67238-119">CommonParameters</span></span>
<span data-ttu-id="67238-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67238-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67238-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67238-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67238-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67238-122">INPUTS</span></span>

## <span data-ttu-id="67238-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67238-123">OUTPUTS</span></span>

### <span data-ttu-id="67238-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="67238-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="67238-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="67238-125">NOTES</span></span>

<span data-ttu-id="67238-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="67238-126">ALIASES</span></span>

## <span data-ttu-id="67238-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67238-127">RELATED LINKS</span></span>

