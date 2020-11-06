---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 420353d7a8af1046456138918092ca56d5c6ed96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497363"
---
# <span data-ttu-id="4bbdc-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bbdc-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="4bbdc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbdc-103">Frissíti az aktuális hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="4bbdc-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bbdc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bbdc-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bbdc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bbdc-105">DESCRIPTION</span></span>
<span data-ttu-id="4bbdc-106">Frissíti az aktuális hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="4bbdc-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="4bbdc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4bbdc-107">EXAMPLES</span></span>

### <span data-ttu-id="4bbdc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4bbdc-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="4bbdc-109">A felügyeleti partner frissítése egy új webhelyre</span><span class="sxs-lookup"><span data-stu-id="4bbdc-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="4bbdc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bbdc-110">PARAMETERS</span></span>

### <span data-ttu-id="4bbdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbdc-111">-DefaultProfile</span></span>
<span data-ttu-id="4bbdc-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bbdc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbdc-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="4bbdc-113">-PartnerId</span></span>
<span data-ttu-id="4bbdc-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="4bbdc-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="4bbdc-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4bbdc-115">-Confirm</span></span>
<span data-ttu-id="4bbdc-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4bbdc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bbdc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bbdc-117">-WhatIf</span></span>
<span data-ttu-id="4bbdc-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4bbdc-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bbdc-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4bbdc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bbdc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbdc-120">CommonParameters</span></span>
<span data-ttu-id="4bbdc-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bbdc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbdc-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbdc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbdc-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bbdc-123">INPUTS</span></span>

### <span data-ttu-id="4bbdc-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="4bbdc-124">None</span></span>

## <span data-ttu-id="4bbdc-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bbdc-125">OUTPUTS</span></span>

### <span data-ttu-id="4bbdc-126">Microsoft. Azure. Command. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bbdc-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="4bbdc-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bbdc-127">NOTES</span></span>

## <span data-ttu-id="4bbdc-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bbdc-128">RELATED LINKS</span></span>

[<span data-ttu-id="4bbdc-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bbdc-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="4bbdc-130">Új – AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bbdc-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="4bbdc-131">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bbdc-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
