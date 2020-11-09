---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297467"
---
# <span data-ttu-id="24732-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="24732-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="24732-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24732-102">SYNOPSIS</span></span>
<span data-ttu-id="24732-103">Új adatmegosztási fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="24732-103">Creates new data share account</span></span>

## <span data-ttu-id="24732-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24732-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24732-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24732-105">DESCRIPTION</span></span>
<span data-ttu-id="24732-106">A **New-AzDataShareAccount** parancsmag létrehoz egy DataShare-fiókot a megadott Azure Resource csoportban.</span><span class="sxs-lookup"><span data-stu-id="24732-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="24732-107">Példák</span><span class="sxs-lookup"><span data-stu-id="24732-107">EXAMPLES</span></span>

### <span data-ttu-id="24732-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24732-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="24732-109">"WikiADS" nevű fiókot hoz létre a "ADS" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="24732-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="24732-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24732-110">PARAMETERS</span></span>

### <span data-ttu-id="24732-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24732-111">-AsJob</span></span>
<span data-ttu-id="24732-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="24732-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="24732-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24732-113">-DefaultProfile</span></span>
<span data-ttu-id="24732-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24732-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24732-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="24732-115">-Location</span></span>
<span data-ttu-id="24732-116">Az a hely, ahová az adatmegosztási fiókot létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="24732-116">The location in which to create the data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24732-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24732-117">-Name</span></span>
<span data-ttu-id="24732-118">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="24732-118">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24732-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24732-119">-ResourceGroupName</span></span>
<span data-ttu-id="24732-120">Létrejön az Azure Data Share-fiók erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="24732-120">The resource group name of the azure data share account will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24732-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="24732-121">-Tag</span></span>
<span data-ttu-id="24732-122">Az Azure Data Share-fiókkal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="24732-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24732-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24732-123">-Confirm</span></span>
<span data-ttu-id="24732-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24732-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24732-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24732-125">-WhatIf</span></span>
<span data-ttu-id="24732-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24732-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24732-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24732-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24732-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24732-128">CommonParameters</span></span>
<span data-ttu-id="24732-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24732-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24732-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="24732-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24732-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24732-131">INPUTS</span></span>

### <span data-ttu-id="24732-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="24732-132">None</span></span>

## <span data-ttu-id="24732-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24732-133">OUTPUTS</span></span>

### <span data-ttu-id="24732-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="24732-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="24732-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24732-135">NOTES</span></span>

## <span data-ttu-id="24732-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24732-136">RELATED LINKS</span></span>
