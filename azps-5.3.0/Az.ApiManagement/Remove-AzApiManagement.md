---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: f54998dc0d5ec8570a573870148a8cf05c265618
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382309"
---
# <span data-ttu-id="8027b-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8027b-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="8027b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8027b-102">SYNOPSIS</span></span>
<span data-ttu-id="8027b-103">Eltávolít egy API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="8027b-103">Removes an API Management service.</span></span>

## <span data-ttu-id="8027b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8027b-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8027b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8027b-105">DESCRIPTION</span></span>
<span data-ttu-id="8027b-106">A **Remove-AzApiManagement** parancsmag eltávolítja az Azure API Management szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="8027b-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="8027b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8027b-107">EXAMPLES</span></span>

### <span data-ttu-id="8027b-108">1. példa: API-kezelési szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8027b-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="8027b-109">Ez a parancs eltávolítja a ContosoApi nevű API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="8027b-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="8027b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8027b-110">PARAMETERS</span></span>

### <span data-ttu-id="8027b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8027b-111">-DefaultProfile</span></span>
<span data-ttu-id="8027b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8027b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8027b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8027b-113">-Name</span></span>
<span data-ttu-id="8027b-114">Annak az API Management-telepítésnek a nevét adja meg, amelyről ez a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="8027b-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8027b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8027b-115">-PassThru</span></span>
<span data-ttu-id="8027b-116">Azt jelzi, hogy ha a művelet sikeres, a parancsmag $True értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8027b-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="8027b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8027b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8027b-118">Annak az erőforráscsoportnak a nevét adja meg, amely alatt az API-kezelési telepítés létezik.</span><span class="sxs-lookup"><span data-stu-id="8027b-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8027b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8027b-119">-Confirm</span></span>
<span data-ttu-id="8027b-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8027b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8027b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8027b-121">-WhatIf</span></span>
<span data-ttu-id="8027b-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8027b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8027b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8027b-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8027b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8027b-124">CommonParameters</span></span>
<span data-ttu-id="8027b-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8027b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8027b-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8027b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8027b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8027b-127">INPUTS</span></span>

### <span data-ttu-id="8027b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8027b-128">System.String</span></span>

## <span data-ttu-id="8027b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8027b-129">OUTPUTS</span></span>

### <span data-ttu-id="8027b-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8027b-130">System.Boolean</span></span>

## <span data-ttu-id="8027b-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8027b-131">NOTES</span></span>

## <span data-ttu-id="8027b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8027b-132">RELATED LINKS</span></span>

[<span data-ttu-id="8027b-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8027b-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="8027b-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8027b-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="8027b-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8027b-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="8027b-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8027b-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


