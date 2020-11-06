---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: a0b6ddf2a5796c63c3efd20b811a2040db123836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504475"
---
# <span data-ttu-id="ac461-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ac461-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="ac461-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac461-102">SYNOPSIS</span></span>
<span data-ttu-id="ac461-103">Hozzáférés visszavonása a lemezhez</span><span class="sxs-lookup"><span data-stu-id="ac461-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac461-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac461-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac461-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac461-105">DESCRIPTION</span></span>
<span data-ttu-id="ac461-106">A **Visszavonás-AzureRmDiskAccess** parancsmag visszavonja a lemezhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="ac461-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="ac461-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ac461-107">EXAMPLES</span></span>

### <span data-ttu-id="ac461-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac461-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="ac461-109">A "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="ac461-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="ac461-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac461-110">PARAMETERS</span></span>

### <span data-ttu-id="ac461-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac461-111">-AsJob</span></span>
<span data-ttu-id="ac461-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ac461-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac461-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac461-113">-DefaultProfile</span></span>
<span data-ttu-id="ac461-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac461-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac461-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ac461-115">-DiskName</span></span>
<span data-ttu-id="ac461-116">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac461-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac461-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac461-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac461-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac461-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac461-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac461-119">-Confirm</span></span>
<span data-ttu-id="ac461-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac461-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac461-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac461-121">-WhatIf</span></span>
<span data-ttu-id="ac461-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac461-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac461-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac461-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac461-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac461-124">CommonParameters</span></span>
<span data-ttu-id="ac461-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac461-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac461-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac461-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac461-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac461-127">INPUTS</span></span>

### <span data-ttu-id="ac461-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ac461-128">System.String</span></span>

## <span data-ttu-id="ac461-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac461-129">OUTPUTS</span></span>

### <span data-ttu-id="ac461-130">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ac461-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ac461-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac461-131">NOTES</span></span>

## <span data-ttu-id="ac461-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac461-132">RELATED LINKS</span></span>
