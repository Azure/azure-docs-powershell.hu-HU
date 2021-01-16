---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377717"
---
# <span data-ttu-id="6cb7e-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="6cb7e-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="6cb7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cb7e-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb7e-103">Biztonsági partner törlése.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-103">Deletes a security contact.</span></span>

## <span data-ttu-id="6cb7e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cb7e-104">SYNTAX</span></span>

### <span data-ttu-id="6cb7e-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cb7e-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb7e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cb7e-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb7e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6cb7e-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cb7e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cb7e-108">DESCRIPTION</span></span>
<span data-ttu-id="6cb7e-109">Biztonsági partner törlése.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-109">Deletes a security contact.</span></span>

## <span data-ttu-id="6cb7e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cb7e-110">EXAMPLES</span></span>

### <span data-ttu-id="6cb7e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6cb7e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="6cb7e-112">Az "alapértelmezett1" biztonsági partner törlése</span><span class="sxs-lookup"><span data-stu-id="6cb7e-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="6cb7e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cb7e-113">PARAMETERS</span></span>

### <span data-ttu-id="6cb7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb7e-114">-DefaultProfile</span></span>
<span data-ttu-id="6cb7e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cb7e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cb7e-116">-InputObject</span></span>
<span data-ttu-id="6cb7e-117">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb7e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6cb7e-118">-Name</span></span>
<span data-ttu-id="6cb7e-119">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb7e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cb7e-120">-PassThru</span></span>
<span data-ttu-id="6cb7e-121">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="6cb7e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cb7e-122">-ResourceId</span></span>
<span data-ttu-id="6cb7e-123">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb7e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cb7e-124">-Confirm</span></span>
<span data-ttu-id="6cb7e-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb7e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb7e-126">-WhatIf</span></span>
<span data-ttu-id="6cb7e-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cb7e-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb7e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb7e-129">CommonParameters</span></span>
<span data-ttu-id="6cb7e-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb7e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb7e-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cb7e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb7e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cb7e-132">INPUTS</span></span>

### <span data-ttu-id="6cb7e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6cb7e-133">System.String</span></span>

### <span data-ttu-id="6cb7e-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="6cb7e-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="6cb7e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cb7e-135">OUTPUTS</span></span>

### <span data-ttu-id="6cb7e-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6cb7e-136">System.Boolean</span></span>

## <span data-ttu-id="6cb7e-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cb7e-137">NOTES</span></span>

## <span data-ttu-id="6cb7e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cb7e-138">RELATED LINKS</span></span>
