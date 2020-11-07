---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 7329889dbc0484e8747b27d49b8781547dcfc256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665929"
---
# <span data-ttu-id="57c75-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="57c75-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="57c75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57c75-102">SYNOPSIS</span></span>
<span data-ttu-id="57c75-103">A Microsoft Partner Network (MPN) AZONOSÍTÓját társítja az aktuális hitelesített felhasználóhoz vagy szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="57c75-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="57c75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57c75-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57c75-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57c75-105">DESCRIPTION</span></span>
<span data-ttu-id="57c75-106">A Microsoft Partner Network (MPN) AZONOSÍTÓját társítja az aktuális hitelesített felhasználóhoz vagy szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="57c75-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="57c75-107">Példák</span><span class="sxs-lookup"><span data-stu-id="57c75-107">EXAMPLES</span></span>

### <span data-ttu-id="57c75-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="57c75-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="57c75-109">Felügyeleti partner felvétele</span><span class="sxs-lookup"><span data-stu-id="57c75-109">Add a management partner</span></span>

## <span data-ttu-id="57c75-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57c75-110">PARAMETERS</span></span>

### <span data-ttu-id="57c75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c75-111">-DefaultProfile</span></span>
<span data-ttu-id="57c75-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57c75-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57c75-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="57c75-113">-PartnerId</span></span>
<span data-ttu-id="57c75-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="57c75-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="57c75-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57c75-115">-Confirm</span></span>
<span data-ttu-id="57c75-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57c75-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57c75-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c75-117">-WhatIf</span></span>
<span data-ttu-id="57c75-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="57c75-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c75-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57c75-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57c75-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c75-120">CommonParameters</span></span>
<span data-ttu-id="57c75-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57c75-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c75-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c75-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c75-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57c75-123">INPUTS</span></span>

### <span data-ttu-id="57c75-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="57c75-124">None</span></span>

## <span data-ttu-id="57c75-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57c75-125">OUTPUTS</span></span>

### <span data-ttu-id="57c75-126">Microsoft. Azure. Command. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="57c75-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="57c75-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57c75-127">NOTES</span></span>

## <span data-ttu-id="57c75-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57c75-128">RELATED LINKS</span></span>

[<span data-ttu-id="57c75-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="57c75-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="57c75-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="57c75-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="57c75-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="57c75-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)