---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187311"
---
# <span data-ttu-id="49a85-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="49a85-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="49a85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49a85-102">SYNOPSIS</span></span>
<span data-ttu-id="49a85-103">Távoli megjelenítési fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="49a85-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="49a85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49a85-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49a85-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="49a85-105">DESCRIPTION</span></span>
<span data-ttu-id="49a85-106">Új távoli megjelenítési fiók létrehozása bizonyos előfizetésekben, erőforrás-csoportokban és-régiókban.</span><span class="sxs-lookup"><span data-stu-id="49a85-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="49a85-107">Példák</span><span class="sxs-lookup"><span data-stu-id="49a85-107">EXAMPLES</span></span>

### <span data-ttu-id="49a85-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="49a85-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="49a85-109">Új távoli megjelenítési fiók létrehozása "példa" a jelenlegi előfizetésben, erőforráscsoport a "rg1" és a közép-amerikai erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="49a85-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="49a85-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49a85-110">PARAMETERS</span></span>

### <span data-ttu-id="49a85-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49a85-111">-Confirm</span></span>
<span data-ttu-id="49a85-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49a85-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a85-113">-DefaultProfile</span></span>
<span data-ttu-id="49a85-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49a85-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a85-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="49a85-115">-Location</span></span>
<span data-ttu-id="49a85-116">Távoli megjelenítési fiók helye.</span><span class="sxs-lookup"><span data-stu-id="49a85-116">Remote Rendering Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a85-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49a85-117">-Name</span></span>
<span data-ttu-id="49a85-118">Távoli megjelenítési fiók neve.</span><span class="sxs-lookup"><span data-stu-id="49a85-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a85-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a85-119">-ResourceGroupName</span></span>
<span data-ttu-id="49a85-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="49a85-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a85-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a85-121">-WhatIf</span></span>
<span data-ttu-id="49a85-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49a85-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a85-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49a85-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a85-124">CommonParameters</span></span>
<span data-ttu-id="49a85-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49a85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="49a85-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a85-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a85-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a85-127">INPUTS</span></span>

### <span data-ttu-id="49a85-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="49a85-128">None</span></span>

## <span data-ttu-id="49a85-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a85-129">OUTPUTS</span></span>

### <span data-ttu-id="49a85-130">Microsoft. Azure. Command. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="49a85-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="49a85-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49a85-131">NOTES</span></span>

## <span data-ttu-id="49a85-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49a85-132">RELATED LINKS</span></span>
