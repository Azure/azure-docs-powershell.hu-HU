---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845469"
---
# <span data-ttu-id="9b2e0-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="9b2e0-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="9b2e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2e0-103">Törölje a Microsoft-Partner Network (MPN) AZONOSÍTÓját az aktuális hitelesített felhasználó vagy szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="9b2e0-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="9b2e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b2e0-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b2e0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b2e0-105">DESCRIPTION</span></span>
<span data-ttu-id="9b2e0-106">Törölje a Microsoft-Partner Network (MPN) AZONOSÍTÓját az aktuális hitelesített felhasználó vagy szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="9b2e0-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="9b2e0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9b2e0-107">EXAMPLES</span></span>

### <span data-ttu-id="9b2e0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9b2e0-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="9b2e0-109">Felügyeleti partner eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9b2e0-109">Remove management partner</span></span>

## <span data-ttu-id="9b2e0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b2e0-110">PARAMETERS</span></span>

### <span data-ttu-id="9b2e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2e0-111">-DefaultProfile</span></span>
<span data-ttu-id="9b2e0-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b2e0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b2e0-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="9b2e0-113">-PartnerId</span></span>
<span data-ttu-id="9b2e0-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="9b2e0-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="9b2e0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b2e0-115">-PassThru</span></span>
<span data-ttu-id="9b2e0-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9b2e0-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9b2e0-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9b2e0-117">-Confirm</span></span>
<span data-ttu-id="9b2e0-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9b2e0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b2e0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b2e0-119">-WhatIf</span></span>
<span data-ttu-id="9b2e0-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9b2e0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b2e0-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b2e0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b2e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2e0-122">CommonParameters</span></span>
<span data-ttu-id="9b2e0-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b2e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2e0-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b2e0-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2e0-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b2e0-125">INPUTS</span></span>

### <span data-ttu-id="9b2e0-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="9b2e0-126">None</span></span>

## <span data-ttu-id="9b2e0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b2e0-127">OUTPUTS</span></span>

### <span data-ttu-id="9b2e0-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b2e0-128">System.Boolean</span></span>

## <span data-ttu-id="9b2e0-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b2e0-129">NOTES</span></span>

## <span data-ttu-id="9b2e0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b2e0-130">RELATED LINKS</span></span>

[<span data-ttu-id="9b2e0-131">Új – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="9b2e0-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="9b2e0-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="9b2e0-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="9b2e0-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="9b2e0-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)