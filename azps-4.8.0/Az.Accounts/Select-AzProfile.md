---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 1ca2244d4ed1a47535a228ed772d9d9a6ecb6acb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180702"
---
# <span data-ttu-id="13b09-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="13b09-101">Select-AzProfile</span></span>

## <span data-ttu-id="13b09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13b09-102">SYNOPSIS</span></span>
<span data-ttu-id="13b09-103">Több szolgáltatásprofilt támogató modulok esetén – a megadott szolgáltatásprofil megfelelő parancsmagok behelyezése.</span><span class="sxs-lookup"><span data-stu-id="13b09-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="13b09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13b09-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13b09-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13b09-105">DESCRIPTION</span></span>
<span data-ttu-id="13b09-106">Több szolgáltatásprofilt támogató modulok esetén – a megadott szolgáltatásprofil megfelelő parancsmagok behelyezése.</span><span class="sxs-lookup"><span data-stu-id="13b09-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="13b09-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13b09-107">EXAMPLES</span></span>

### <span data-ttu-id="13b09-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13b09-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="13b09-109">A AzureStack-profil parancsmagjának beolvasása március 2019</span><span class="sxs-lookup"><span data-stu-id="13b09-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="13b09-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13b09-110">PARAMETERS</span></span>

### <span data-ttu-id="13b09-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13b09-111">-Name</span></span>
<span data-ttu-id="13b09-112">A kijelölni kívánt profil neve</span><span class="sxs-lookup"><span data-stu-id="13b09-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b09-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13b09-113">-PassThru</span></span>
<span data-ttu-id="13b09-114">Ha van, kényszeríti a parancsmagot a sikeres végrehajtás értékének visszaadására.</span><span class="sxs-lookup"><span data-stu-id="13b09-114">When present, forces the cmdlet to return a value on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b09-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13b09-115">-Confirm</span></span>
<span data-ttu-id="13b09-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13b09-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b09-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b09-117">-WhatIf</span></span>
<span data-ttu-id="13b09-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13b09-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13b09-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13b09-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b09-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b09-120">CommonParameters</span></span>
<span data-ttu-id="13b09-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13b09-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b09-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13b09-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b09-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13b09-123">INPUTS</span></span>

### <span data-ttu-id="13b09-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="13b09-124">None</span></span>

## <span data-ttu-id="13b09-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13b09-125">OUTPUTS</span></span>

### <span data-ttu-id="13b09-126">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="13b09-126">System.Object</span></span>
## <span data-ttu-id="13b09-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13b09-127">NOTES</span></span>

## <span data-ttu-id="13b09-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13b09-128">RELATED LINKS</span></span>
