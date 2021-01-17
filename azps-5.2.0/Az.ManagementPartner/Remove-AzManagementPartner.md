---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329500"
---
# <span data-ttu-id="0f708-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0f708-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="0f708-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f708-102">SYNOPSIS</span></span>
<span data-ttu-id="0f708-103">Törölje az aktuálisan hitelesített felhasználó vagy egyszerű szolgáltatásnév Microsoft Partner Network(MPN) azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="0f708-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0f708-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f708-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f708-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f708-105">DESCRIPTION</span></span>
<span data-ttu-id="0f708-106">Törölje az aktuálisan hitelesített felhasználó vagy egyszerű szolgáltatásnév Microsoft Partner Network(MPN) azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="0f708-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0f708-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f708-107">EXAMPLES</span></span>

### <span data-ttu-id="0f708-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0f708-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="0f708-109">Felügyeleti partner eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0f708-109">Remove management partner</span></span>

## <span data-ttu-id="0f708-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f708-110">PARAMETERS</span></span>

### <span data-ttu-id="0f708-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f708-111">-DefaultProfile</span></span>
<span data-ttu-id="0f708-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f708-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f708-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="0f708-113">-PartnerId</span></span>
<span data-ttu-id="0f708-114">A vezető partner azonosítója, ez egy 6 jegyű szám.</span><span class="sxs-lookup"><span data-stu-id="0f708-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="0f708-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f708-115">-PassThru</span></span>
<span data-ttu-id="0f708-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0f708-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0f708-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f708-117">-Confirm</span></span>
<span data-ttu-id="0f708-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0f708-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f708-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f708-119">-WhatIf</span></span>
<span data-ttu-id="0f708-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0f708-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f708-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f708-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f708-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f708-122">CommonParameters</span></span>
<span data-ttu-id="0f708-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f708-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f708-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f708-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f708-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f708-125">INPUTS</span></span>

### <span data-ttu-id="0f708-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="0f708-126">None</span></span>

## <span data-ttu-id="0f708-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f708-127">OUTPUTS</span></span>

### <span data-ttu-id="0f708-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f708-128">System.Boolean</span></span>

## <span data-ttu-id="0f708-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f708-129">NOTES</span></span>

## <span data-ttu-id="0f708-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f708-130">RELATED LINKS</span></span>

[<span data-ttu-id="0f708-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0f708-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="0f708-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0f708-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="0f708-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0f708-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)