---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/get-azurermmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
ms.openlocfilehash: d291814a2683388fd6c8fa7b26e06195e9cfa09d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680068"
---
# <span data-ttu-id="31e8c-101">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31e8c-101">Get-AzureRmManagementPartner</span></span>

## <span data-ttu-id="31e8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="31e8c-103">Az aktuálisan hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) azonosítójának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="31e8c-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31e8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31e8c-104">SYNTAX</span></span>

```
Get-AzureRmManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31e8c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="31e8c-106">Az aktuálisan hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) azonosítójának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="31e8c-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

## <span data-ttu-id="31e8c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="31e8c-107">EXAMPLES</span></span>

### <span data-ttu-id="31e8c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="31e8c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="31e8c-109">A jelenlegi felügyeleti partner azonosítójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="31e8c-109">Get the current management partner id</span></span>

### <span data-ttu-id="31e8c-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="31e8c-110">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="31e8c-111">A jelenlegi kezelési partnerek azonosítójának beszerzése partner-azonosítóval (ha nem egyeznek meg), sikertelen lesz</span><span class="sxs-lookup"><span data-stu-id="31e8c-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="31e8c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31e8c-112">PARAMETERS</span></span>

### <span data-ttu-id="31e8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e8c-113">-DefaultProfile</span></span>
<span data-ttu-id="31e8c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31e8c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31e8c-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="31e8c-115">-PartnerId</span></span>
<span data-ttu-id="31e8c-116">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="31e8c-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e8c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e8c-117">CommonParameters</span></span>
<span data-ttu-id="31e8c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31e8c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e8c-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e8c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e8c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31e8c-120">INPUTS</span></span>

### <span data-ttu-id="31e8c-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="31e8c-121">None</span></span>

## <span data-ttu-id="31e8c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31e8c-122">OUTPUTS</span></span>

### <span data-ttu-id="31e8c-123">Microsoft. Azure. Command. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31e8c-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="31e8c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31e8c-124">NOTES</span></span>

## <span data-ttu-id="31e8c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31e8c-125">RELATED LINKS</span></span>

[<span data-ttu-id="31e8c-126">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31e8c-126">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="31e8c-127">Új – AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31e8c-127">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="31e8c-128">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31e8c-128">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
