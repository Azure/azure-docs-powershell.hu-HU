---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 04b98f15def219c269bf18f21fb371822cc97f6d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841013"
---
# <span data-ttu-id="e0c80-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="e0c80-101">Select-AzProfile</span></span>

## <span data-ttu-id="e0c80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0c80-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c80-103">Több szolgáltatásprofilt támogató modulok esetén – a megadott szolgáltatásprofil megfelelő parancsmagok behelyezése.</span><span class="sxs-lookup"><span data-stu-id="e0c80-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="e0c80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0c80-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0c80-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0c80-105">DESCRIPTION</span></span>
<span data-ttu-id="e0c80-106">Több szolgáltatásprofilt támogató modulok esetén – a megadott szolgáltatásprofil megfelelő parancsmagok behelyezése.</span><span class="sxs-lookup"><span data-stu-id="e0c80-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="e0c80-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0c80-107">EXAMPLES</span></span>

### <span data-ttu-id="e0c80-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e0c80-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="e0c80-109">A AzureStack-profil parancsmagjának beolvasása március 2019</span><span class="sxs-lookup"><span data-stu-id="e0c80-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="e0c80-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0c80-110">PARAMETERS</span></span>

### <span data-ttu-id="e0c80-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0c80-111">-Name</span></span>
<span data-ttu-id="e0c80-112">A kijelölni kívánt profil neve</span><span class="sxs-lookup"><span data-stu-id="e0c80-112">The name of the profile to select</span></span>

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

### <span data-ttu-id="e0c80-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0c80-113">-PassThru</span></span>
<span data-ttu-id="e0c80-114">Ha van, kényszeríti a parancsmagot a sikeres végrehajtás értékének visszaadására.</span><span class="sxs-lookup"><span data-stu-id="e0c80-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="e0c80-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0c80-115">-Confirm</span></span>
<span data-ttu-id="e0c80-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0c80-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0c80-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0c80-117">-WhatIf</span></span>
<span data-ttu-id="e0c80-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0c80-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0c80-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0c80-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0c80-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c80-120">CommonParameters</span></span>
<span data-ttu-id="e0c80-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0c80-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c80-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0c80-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c80-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0c80-123">INPUTS</span></span>

### <span data-ttu-id="e0c80-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="e0c80-124">None</span></span>

## <span data-ttu-id="e0c80-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0c80-125">OUTPUTS</span></span>

### <span data-ttu-id="e0c80-126">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="e0c80-126">System.Object</span></span>
## <span data-ttu-id="e0c80-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0c80-127">NOTES</span></span>

## <span data-ttu-id="e0c80-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0c80-128">RELATED LINKS</span></span>
