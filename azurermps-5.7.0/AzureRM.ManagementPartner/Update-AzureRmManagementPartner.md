---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 9d1694cdde3edd94112fc5b1960fd870b842d6e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673044"
---
# <span data-ttu-id="a011a-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a011a-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="a011a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a011a-102">SYNOPSIS</span></span>
<span data-ttu-id="a011a-103">Frissíti az aktuális hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="a011a-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a011a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a011a-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a011a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a011a-105">DESCRIPTION</span></span>
<span data-ttu-id="a011a-106">Frissíti az aktuális hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="a011a-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a011a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a011a-107">EXAMPLES</span></span>

### <span data-ttu-id="a011a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a011a-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="a011a-109">A felügyeleti partner frissítése egy új webhelyre</span><span class="sxs-lookup"><span data-stu-id="a011a-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="a011a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a011a-110">PARAMETERS</span></span>

### <span data-ttu-id="a011a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a011a-111">-DefaultProfile</span></span>
<span data-ttu-id="a011a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a011a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a011a-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="a011a-113">-PartnerId</span></span>
<span data-ttu-id="a011a-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="a011a-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a011a-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a011a-115">-Confirm</span></span>
<span data-ttu-id="a011a-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a011a-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a011a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a011a-117">-WhatIf</span></span>
<span data-ttu-id="a011a-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a011a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a011a-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a011a-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a011a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a011a-120">CommonParameters</span></span>
<span data-ttu-id="a011a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a011a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a011a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a011a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a011a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a011a-123">INPUTS</span></span>

### <span data-ttu-id="a011a-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="a011a-124">None</span></span>

## <span data-ttu-id="a011a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a011a-125">OUTPUTS</span></span>

### <span data-ttu-id="a011a-126">Microsoft. Azure. Command. Resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a011a-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="a011a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a011a-127">NOTES</span></span>

## <span data-ttu-id="a011a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a011a-128">RELATED LINKS</span></span>

[<span data-ttu-id="a011a-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a011a-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="a011a-130">Új – AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a011a-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="a011a-131">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a011a-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
