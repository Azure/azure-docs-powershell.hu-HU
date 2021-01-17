---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480451"
---
# <span data-ttu-id="545af-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="545af-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="545af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="545af-102">SYNOPSIS</span></span>
<span data-ttu-id="545af-103">Új jelszót állít be egy felhasználónak az eszközön.</span><span class="sxs-lookup"><span data-stu-id="545af-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="545af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="545af-104">SYNTAX</span></span>

### <span data-ttu-id="545af-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="545af-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545af-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="545af-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545af-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="545af-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545af-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="545af-108">DESCRIPTION</span></span>
<span data-ttu-id="545af-109">A **Set-AzDataBoxEdgeUser** parancsmag új jelszót állít be egy felhasználónak az Adatmező Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="545af-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="545af-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="545af-110">EXAMPLES</span></span>

### <span data-ttu-id="545af-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="545af-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="545af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="545af-112">PARAMETERS</span></span>

### <span data-ttu-id="545af-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="545af-113">-AsJob</span></span>
<span data-ttu-id="545af-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="545af-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="545af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545af-115">-DefaultProfile</span></span>
<span data-ttu-id="545af-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="545af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="545af-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="545af-117">-DeviceName</span></span>
<span data-ttu-id="545af-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="545af-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545af-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="545af-119">-EncryptionKey</span></span>
<span data-ttu-id="545af-120">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="545af-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="545af-121">-InputObject</span></span>
<span data-ttu-id="545af-122">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="545af-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545af-123">-Name</span><span class="sxs-lookup"><span data-stu-id="545af-123">-Name</span></span>
<span data-ttu-id="545af-124">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="545af-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545af-125">-Password</span><span class="sxs-lookup"><span data-stu-id="545af-125">-Password</span></span>
<span data-ttu-id="545af-126">Jelszó megadása biztonságos karakterláncként</span><span class="sxs-lookup"><span data-stu-id="545af-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545af-127">-ResourceGroupName</span></span>
<span data-ttu-id="545af-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="545af-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545af-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="545af-129">-ResourceId</span></span>
<span data-ttu-id="545af-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="545af-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545af-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="545af-131">-Confirm</span></span>
<span data-ttu-id="545af-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="545af-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="545af-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545af-133">-WhatIf</span></span>
<span data-ttu-id="545af-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="545af-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="545af-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="545af-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="545af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545af-136">CommonParameters</span></span>
<span data-ttu-id="545af-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="545af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545af-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="545af-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545af-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="545af-139">INPUTS</span></span>

### <span data-ttu-id="545af-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="545af-140">None</span></span>

## <span data-ttu-id="545af-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="545af-141">OUTPUTS</span></span>

### <span data-ttu-id="545af-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="545af-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="545af-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="545af-143">NOTES</span></span>

## <span data-ttu-id="545af-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="545af-144">RELATED LINKS</span></span>
