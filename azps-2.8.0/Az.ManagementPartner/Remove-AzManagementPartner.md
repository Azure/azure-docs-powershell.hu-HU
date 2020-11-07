---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: 5910d82ddee49ba47c709a3323f72e325f4067ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665926"
---
# <span data-ttu-id="cc0b0-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cc0b0-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="cc0b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="cc0b0-103">Törölje a Microsoft-Partner Network (MPN) AZONOSÍTÓját az aktuális hitelesített felhasználó vagy szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="cc0b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc0b0-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc0b0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc0b0-105">DESCRIPTION</span></span>
<span data-ttu-id="cc0b0-106">Törölje a Microsoft-Partner Network (MPN) AZONOSÍTÓját az aktuális hitelesített felhasználó vagy szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="cc0b0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cc0b0-107">EXAMPLES</span></span>

### <span data-ttu-id="cc0b0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cc0b0-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="cc0b0-109">Felügyeleti partner eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cc0b0-109">Remove management partner</span></span>

## <span data-ttu-id="cc0b0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc0b0-110">PARAMETERS</span></span>

### <span data-ttu-id="cc0b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc0b0-111">-DefaultProfile</span></span>
<span data-ttu-id="cc0b0-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc0b0-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="cc0b0-113">-PartnerId</span></span>
<span data-ttu-id="cc0b0-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="cc0b0-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc0b0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc0b0-115">-PassThru</span></span>
<span data-ttu-id="cc0b0-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cc0b0-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cc0b0-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc0b0-117">-Confirm</span></span>
<span data-ttu-id="cc0b0-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc0b0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc0b0-119">-WhatIf</span></span>
<span data-ttu-id="cc0b0-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc0b0-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc0b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc0b0-122">CommonParameters</span></span>
<span data-ttu-id="cc0b0-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc0b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc0b0-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc0b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc0b0-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc0b0-125">INPUTS</span></span>

### <span data-ttu-id="cc0b0-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="cc0b0-126">None</span></span>

## <span data-ttu-id="cc0b0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc0b0-127">OUTPUTS</span></span>

### <span data-ttu-id="cc0b0-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc0b0-128">System.Boolean</span></span>

## <span data-ttu-id="cc0b0-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc0b0-129">NOTES</span></span>

## <span data-ttu-id="cc0b0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc0b0-130">RELATED LINKS</span></span>

[<span data-ttu-id="cc0b0-131">Új – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cc0b0-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="cc0b0-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cc0b0-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="cc0b0-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cc0b0-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)