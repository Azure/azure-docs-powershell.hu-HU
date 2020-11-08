---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187691"
---
# <span data-ttu-id="b2d3f-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b2d3f-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="b2d3f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d3f-103">Törölje a Microsoft-Partner Network (MPN) AZONOSÍTÓját az aktuális hitelesített felhasználó vagy szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b2d3f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2d3f-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2d3f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d3f-106">Törölje a Microsoft-Partner Network (MPN) AZONOSÍTÓját az aktuális hitelesített felhasználó vagy szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b2d3f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b2d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="b2d3f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b2d3f-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="b2d3f-109">Felügyeleti partner eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b2d3f-109">Remove management partner</span></span>

## <span data-ttu-id="b2d3f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2d3f-110">PARAMETERS</span></span>

### <span data-ttu-id="b2d3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d3f-111">-DefaultProfile</span></span>
<span data-ttu-id="b2d3f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2d3f-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="b2d3f-113">-PartnerId</span></span>
<span data-ttu-id="b2d3f-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="b2d3f-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="b2d3f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2d3f-115">-PassThru</span></span>
<span data-ttu-id="b2d3f-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b2d3f-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b2d3f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b2d3f-117">-Confirm</span></span>
<span data-ttu-id="b2d3f-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d3f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d3f-119">-WhatIf</span></span>
<span data-ttu-id="b2d3f-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2d3f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d3f-122">CommonParameters</span></span>
<span data-ttu-id="b2d3f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2d3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d3f-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d3f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2d3f-125">INPUTS</span></span>

### <span data-ttu-id="b2d3f-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="b2d3f-126">None</span></span>

## <span data-ttu-id="b2d3f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2d3f-127">OUTPUTS</span></span>

### <span data-ttu-id="b2d3f-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2d3f-128">System.Boolean</span></span>

## <span data-ttu-id="b2d3f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2d3f-129">NOTES</span></span>

## <span data-ttu-id="b2d3f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2d3f-130">RELATED LINKS</span></span>

[<span data-ttu-id="b2d3f-131">Új – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b2d3f-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="b2d3f-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b2d3f-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="b2d3f-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b2d3f-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)