---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187328"
---
# <span data-ttu-id="f5649-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f5649-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="f5649-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5649-102">SYNOPSIS</span></span>
<span data-ttu-id="f5649-103">A Microsoft Partner Network (MPN) AZONOSÍTÓját társítja az aktuális hitelesített felhasználóhoz vagy szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f5649-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="f5649-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5649-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5649-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5649-105">DESCRIPTION</span></span>
<span data-ttu-id="f5649-106">A Microsoft Partner Network (MPN) AZONOSÍTÓját társítja az aktuális hitelesített felhasználóhoz vagy szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f5649-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="f5649-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f5649-107">EXAMPLES</span></span>

### <span data-ttu-id="f5649-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f5649-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="f5649-109">Felügyeleti partner felvétele</span><span class="sxs-lookup"><span data-stu-id="f5649-109">Add a management partner</span></span>

## <span data-ttu-id="f5649-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5649-110">PARAMETERS</span></span>

### <span data-ttu-id="f5649-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5649-111">-DefaultProfile</span></span>
<span data-ttu-id="f5649-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5649-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5649-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="f5649-113">-PartnerId</span></span>
<span data-ttu-id="f5649-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="f5649-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="f5649-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5649-115">-Confirm</span></span>
<span data-ttu-id="f5649-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5649-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5649-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5649-117">-WhatIf</span></span>
<span data-ttu-id="f5649-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5649-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5649-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5649-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5649-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5649-120">CommonParameters</span></span>
<span data-ttu-id="f5649-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5649-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5649-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5649-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5649-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5649-123">INPUTS</span></span>

### <span data-ttu-id="f5649-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="f5649-124">None</span></span>

## <span data-ttu-id="f5649-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5649-125">OUTPUTS</span></span>

### <span data-ttu-id="f5649-126">Microsoft. Azure. Command. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f5649-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="f5649-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5649-127">NOTES</span></span>

## <span data-ttu-id="f5649-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5649-128">RELATED LINKS</span></span>

[<span data-ttu-id="f5649-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f5649-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="f5649-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f5649-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="f5649-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f5649-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)