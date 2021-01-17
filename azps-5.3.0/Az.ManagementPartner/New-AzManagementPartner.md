---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467634"
---
# <span data-ttu-id="990ab-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="990ab-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="990ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="990ab-102">SYNOPSIS</span></span>
<span data-ttu-id="990ab-103">Egy Microsoft Partner Network(MPN) azonosítót társít az aktuálisan hitelesített felhasználóhoz vagy szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="990ab-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="990ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="990ab-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="990ab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="990ab-105">DESCRIPTION</span></span>
<span data-ttu-id="990ab-106">Egy Microsoft Partner Network(MPN) azonosítót társít az aktuálisan hitelesített felhasználóhoz vagy szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="990ab-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="990ab-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="990ab-107">EXAMPLES</span></span>

### <span data-ttu-id="990ab-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="990ab-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="990ab-109">Felügyeleti partner hozzáadása</span><span class="sxs-lookup"><span data-stu-id="990ab-109">Add a management partner</span></span>

## <span data-ttu-id="990ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="990ab-110">PARAMETERS</span></span>

### <span data-ttu-id="990ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="990ab-111">-DefaultProfile</span></span>
<span data-ttu-id="990ab-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="990ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="990ab-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="990ab-113">-PartnerId</span></span>
<span data-ttu-id="990ab-114">A vezető partner azonosítója, ez egy 6 jegyű szám.</span><span class="sxs-lookup"><span data-stu-id="990ab-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="990ab-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="990ab-115">-Confirm</span></span>
<span data-ttu-id="990ab-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="990ab-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="990ab-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="990ab-117">-WhatIf</span></span>
<span data-ttu-id="990ab-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="990ab-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="990ab-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="990ab-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="990ab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="990ab-120">CommonParameters</span></span>
<span data-ttu-id="990ab-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="990ab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="990ab-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="990ab-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="990ab-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="990ab-123">INPUTS</span></span>

### <span data-ttu-id="990ab-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="990ab-124">None</span></span>

## <span data-ttu-id="990ab-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="990ab-125">OUTPUTS</span></span>

### <span data-ttu-id="990ab-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="990ab-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="990ab-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="990ab-127">NOTES</span></span>

## <span data-ttu-id="990ab-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="990ab-128">RELATED LINKS</span></span>

[<span data-ttu-id="990ab-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="990ab-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="990ab-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="990ab-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="990ab-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="990ab-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)