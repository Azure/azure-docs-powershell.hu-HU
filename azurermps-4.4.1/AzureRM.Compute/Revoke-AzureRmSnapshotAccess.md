---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: 6d7b41ae7250a294b86333ecf2926a2eda06d3bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672064"
---
# <span data-ttu-id="fdcd6-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="fdcd6-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="fdcd6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdcd6-102">SYNOPSIS</span></span>
<span data-ttu-id="fdcd6-103">A pillanatképhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="fdcd6-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdcd6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdcd6-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdcd6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdcd6-105">DESCRIPTION</span></span>
<span data-ttu-id="fdcd6-106">A **Visszavonás-AzureRmSnapshotAccess** parancsmag visszavonja a pillanatképhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="fdcd6-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="fdcd6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fdcd6-107">EXAMPLES</span></span>

### <span data-ttu-id="fdcd6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fdcd6-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="fdcd6-109">A "ResourceGroup01" nevű erőforráscsoport "Snapshot01" nevű pillanatképéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="fdcd6-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="fdcd6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdcd6-110">PARAMETERS</span></span>

### <span data-ttu-id="fdcd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdcd6-111">-DefaultProfile</span></span>
<span data-ttu-id="fdcd6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdcd6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdcd6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdcd6-113">-ResourceGroupName</span></span>
<span data-ttu-id="fdcd6-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdcd6-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fdcd6-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="fdcd6-115">-SnapshotName</span></span>
<span data-ttu-id="fdcd6-116">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdcd6-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="fdcd6-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fdcd6-117">-Confirm</span></span>
<span data-ttu-id="fdcd6-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fdcd6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdcd6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdcd6-119">-WhatIf</span></span>
<span data-ttu-id="fdcd6-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fdcd6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdcd6-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fdcd6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdcd6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdcd6-122">CommonParameters</span></span>
<span data-ttu-id="fdcd6-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdcd6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdcd6-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdcd6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdcd6-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdcd6-125">INPUTS</span></span>

### <span data-ttu-id="fdcd6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fdcd6-126">System.String</span></span>

## <span data-ttu-id="fdcd6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdcd6-127">OUTPUTS</span></span>

### <span data-ttu-id="fdcd6-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="fdcd6-128">System.Object</span></span>

## <span data-ttu-id="fdcd6-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdcd6-129">NOTES</span></span>

## <span data-ttu-id="fdcd6-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdcd6-130">RELATED LINKS</span></span>

