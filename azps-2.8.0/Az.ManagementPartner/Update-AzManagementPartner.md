---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 20d258cdd99da4e76fcf8394ebbe1aadd54f2fb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665925"
---
# <span data-ttu-id="cb124-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cb124-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="cb124-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb124-102">SYNOPSIS</span></span>
<span data-ttu-id="cb124-103">Frissíti az aktuális hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="cb124-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="cb124-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb124-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb124-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb124-105">DESCRIPTION</span></span>
<span data-ttu-id="cb124-106">Frissíti az aktuális hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="cb124-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="cb124-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cb124-107">EXAMPLES</span></span>

### <span data-ttu-id="cb124-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cb124-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="cb124-109">A felügyeleti partner frissítése egy új webhelyre</span><span class="sxs-lookup"><span data-stu-id="cb124-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="cb124-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb124-110">PARAMETERS</span></span>

### <span data-ttu-id="cb124-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb124-111">-DefaultProfile</span></span>
<span data-ttu-id="cb124-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb124-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb124-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="cb124-113">-PartnerId</span></span>
<span data-ttu-id="cb124-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="cb124-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="cb124-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb124-115">-Confirm</span></span>
<span data-ttu-id="cb124-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb124-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb124-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb124-117">-WhatIf</span></span>
<span data-ttu-id="cb124-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb124-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb124-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb124-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb124-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb124-120">CommonParameters</span></span>
<span data-ttu-id="cb124-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb124-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb124-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb124-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb124-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb124-123">INPUTS</span></span>

### <span data-ttu-id="cb124-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="cb124-124">None</span></span>

## <span data-ttu-id="cb124-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb124-125">OUTPUTS</span></span>

### <span data-ttu-id="cb124-126">Microsoft. Azure. Command. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cb124-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="cb124-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb124-127">NOTES</span></span>

## <span data-ttu-id="cb124-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb124-128">RELATED LINKS</span></span>

[<span data-ttu-id="cb124-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cb124-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="cb124-130">Új – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cb124-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="cb124-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cb124-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)