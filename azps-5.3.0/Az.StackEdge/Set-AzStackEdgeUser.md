---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374273"
---
# <span data-ttu-id="9c625-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9c625-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="9c625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c625-102">SYNOPSIS</span></span>
<span data-ttu-id="9c625-103">Új jelszót állít be egy felhasználónak az eszközön.</span><span class="sxs-lookup"><span data-stu-id="9c625-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="9c625-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9c625-104">SYNTAX</span></span>

### <span data-ttu-id="9c625-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c625-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c625-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c625-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c625-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c625-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c625-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9c625-108">DESCRIPTION</span></span>
<span data-ttu-id="9c625-109">A **Set-AzStackEdgeUser** parancsmag új jelszót állít be egy felhasználónak a Stack Edge eszközön.</span><span class="sxs-lookup"><span data-stu-id="9c625-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="9c625-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9c625-110">EXAMPLES</span></span>

### <span data-ttu-id="9c625-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9c625-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="9c625-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c625-112">PARAMETERS</span></span>

### <span data-ttu-id="9c625-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c625-113">-AsJob</span></span>
<span data-ttu-id="9c625-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9c625-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c625-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c625-115">-DefaultProfile</span></span>
<span data-ttu-id="9c625-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c625-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c625-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9c625-117">-DeviceName</span></span>
<span data-ttu-id="9c625-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="9c625-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c625-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9c625-119">-EncryptionKey</span></span>
<span data-ttu-id="9c625-120">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="9c625-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="9c625-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c625-121">-InputObject</span></span>
<span data-ttu-id="9c625-122">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="9c625-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c625-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9c625-123">-Name</span></span>
<span data-ttu-id="9c625-124">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="9c625-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c625-125">-Password</span><span class="sxs-lookup"><span data-stu-id="9c625-125">-Password</span></span>
<span data-ttu-id="9c625-126">Jelszó megadása biztonságos karakterláncként</span><span class="sxs-lookup"><span data-stu-id="9c625-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="9c625-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c625-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c625-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9c625-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c625-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c625-129">-ResourceId</span></span>
<span data-ttu-id="9c625-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c625-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c625-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c625-131">-Confirm</span></span>
<span data-ttu-id="9c625-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9c625-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c625-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c625-133">-WhatIf</span></span>
<span data-ttu-id="9c625-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9c625-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c625-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c625-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c625-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c625-136">CommonParameters</span></span>
<span data-ttu-id="9c625-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c625-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c625-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c625-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c625-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c625-139">INPUTS</span></span>

### <span data-ttu-id="9c625-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="9c625-140">None</span></span>

## <span data-ttu-id="9c625-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c625-141">OUTPUTS</span></span>

### <span data-ttu-id="9c625-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9c625-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="9c625-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9c625-143">NOTES</span></span>

## <span data-ttu-id="9c625-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c625-144">RELATED LINKS</span></span>
