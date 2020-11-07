---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: c3a783178bf8342e891f8eab2996e77a2045721a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679264"
---
# <span data-ttu-id="f0840-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="f0840-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="f0840-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0840-102">SYNOPSIS</span></span>
<span data-ttu-id="f0840-103">Csoporttagokat szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="f0840-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0840-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0840-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0840-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0840-105">DESCRIPTION</span></span>
<span data-ttu-id="f0840-106">Csoporttagokat szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="f0840-106">Get a group members.</span></span>

## <span data-ttu-id="f0840-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f0840-107">EXAMPLES</span></span>

### <span data-ttu-id="f0840-108">Csoporttagok szűrése csoport objektum-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="f0840-108">Filters group members using group object id</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="f0840-109">A csoporttagok bekerülnek a 85F89C90-780E-4AA6-9F4F-6F268D322EEE-azonosítójával</span><span class="sxs-lookup"><span data-stu-id="f0840-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="f0840-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0840-110">PARAMETERS</span></span>

### <span data-ttu-id="f0840-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0840-111">-DefaultProfile</span></span>
<span data-ttu-id="f0840-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f0840-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0840-113">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="f0840-113">-GroupObjectId</span></span>
<span data-ttu-id="f0840-114">A csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f0840-114">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0840-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0840-115">CommonParameters</span></span>
<span data-ttu-id="f0840-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0840-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0840-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0840-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0840-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0840-118">INPUTS</span></span>

### <span data-ttu-id="f0840-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="f0840-119">None</span></span>
<span data-ttu-id="f0840-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f0840-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0840-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0840-121">OUTPUTS</span></span>

### <span data-ttu-id="f0840-122">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject]</span><span class="sxs-lookup"><span data-stu-id="f0840-122">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="f0840-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0840-123">NOTES</span></span>

## <span data-ttu-id="f0840-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0840-124">RELATED LINKS</span></span>

[<span data-ttu-id="f0840-125">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f0840-125">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="f0840-126">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f0840-126">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

