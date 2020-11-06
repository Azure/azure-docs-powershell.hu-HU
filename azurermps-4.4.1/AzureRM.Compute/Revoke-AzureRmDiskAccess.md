---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 58cbbfd2314589fd6b28f2ff375aa268c39e63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492525"
---
# <span data-ttu-id="5aad5-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5aad5-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="5aad5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5aad5-102">SYNOPSIS</span></span>
<span data-ttu-id="5aad5-103">Hozzáférés visszavonása a lemezhez</span><span class="sxs-lookup"><span data-stu-id="5aad5-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aad5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5aad5-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aad5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5aad5-105">DESCRIPTION</span></span>
<span data-ttu-id="5aad5-106">A **Visszavonás-AzureRmDiskAccess** parancsmag visszavonja a lemezhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="5aad5-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="5aad5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5aad5-107">EXAMPLES</span></span>

### <span data-ttu-id="5aad5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5aad5-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="5aad5-109">A "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="5aad5-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="5aad5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5aad5-110">PARAMETERS</span></span>

### <span data-ttu-id="5aad5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aad5-111">-DefaultProfile</span></span>
<span data-ttu-id="5aad5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5aad5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5aad5-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="5aad5-113">-DiskName</span></span>
<span data-ttu-id="5aad5-114">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5aad5-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="5aad5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aad5-115">-ResourceGroupName</span></span>
<span data-ttu-id="5aad5-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5aad5-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5aad5-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5aad5-117">-Confirm</span></span>
<span data-ttu-id="5aad5-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5aad5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aad5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aad5-119">-WhatIf</span></span>
<span data-ttu-id="5aad5-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5aad5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5aad5-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5aad5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aad5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aad5-122">CommonParameters</span></span>
<span data-ttu-id="5aad5-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5aad5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aad5-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aad5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aad5-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5aad5-125">INPUTS</span></span>

### <span data-ttu-id="5aad5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5aad5-126">System.String</span></span>

## <span data-ttu-id="5aad5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5aad5-127">OUTPUTS</span></span>

### <span data-ttu-id="5aad5-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5aad5-128">System.Object</span></span>

## <span data-ttu-id="5aad5-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5aad5-129">NOTES</span></span>

## <span data-ttu-id="5aad5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5aad5-130">RELATED LINKS</span></span>

