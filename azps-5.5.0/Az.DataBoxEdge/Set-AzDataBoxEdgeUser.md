---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162082"
---
# <span data-ttu-id="1eb17-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="1eb17-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="1eb17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eb17-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb17-103">Új jelszót állít be egy felhasználónak az eszközön.</span><span class="sxs-lookup"><span data-stu-id="1eb17-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="1eb17-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1eb17-104">SYNTAX</span></span>

### <span data-ttu-id="1eb17-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1eb17-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb17-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb17-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb17-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1eb17-108">DESCRIPTION</span></span>
<span data-ttu-id="1eb17-109">A **Set-AzDataBoxEdgeUser** parancsmag új jelszót állít be egy felhasználónak az Adatmező Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="1eb17-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="1eb17-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1eb17-110">EXAMPLES</span></span>

### <span data-ttu-id="1eb17-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1eb17-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="1eb17-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1eb17-112">PARAMETERS</span></span>

### <span data-ttu-id="1eb17-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1eb17-113">-AsJob</span></span>
<span data-ttu-id="1eb17-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1eb17-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1eb17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb17-115">-DefaultProfile</span></span>
<span data-ttu-id="1eb17-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1eb17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb17-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1eb17-117">-DeviceName</span></span>
<span data-ttu-id="1eb17-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="1eb17-118">Device Name</span></span>

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

### <span data-ttu-id="1eb17-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1eb17-119">-EncryptionKey</span></span>
<span data-ttu-id="1eb17-120">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="1eb17-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="1eb17-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1eb17-121">-InputObject</span></span>
<span data-ttu-id="1eb17-122">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="1eb17-122">Input Object</span></span>

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

### <span data-ttu-id="1eb17-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1eb17-123">-Name</span></span>
<span data-ttu-id="1eb17-124">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="1eb17-124">Username</span></span>

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

### <span data-ttu-id="1eb17-125">-Password</span><span class="sxs-lookup"><span data-stu-id="1eb17-125">-Password</span></span>
<span data-ttu-id="1eb17-126">Jelszó megadása biztonságos karakterláncként</span><span class="sxs-lookup"><span data-stu-id="1eb17-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="1eb17-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb17-127">-ResourceGroupName</span></span>
<span data-ttu-id="1eb17-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1eb17-128">Resource Group Name</span></span>

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

### <span data-ttu-id="1eb17-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eb17-129">-ResourceId</span></span>
<span data-ttu-id="1eb17-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eb17-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="1eb17-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eb17-131">-Confirm</span></span>
<span data-ttu-id="1eb17-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1eb17-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb17-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb17-133">-WhatIf</span></span>
<span data-ttu-id="1eb17-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1eb17-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1eb17-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1eb17-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb17-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb17-136">CommonParameters</span></span>
<span data-ttu-id="1eb17-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb17-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb17-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1eb17-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb17-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1eb17-139">INPUTS</span></span>

### <span data-ttu-id="1eb17-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="1eb17-140">None</span></span>

## <span data-ttu-id="1eb17-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1eb17-141">OUTPUTS</span></span>

### <span data-ttu-id="1eb17-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="1eb17-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="1eb17-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1eb17-143">NOTES</span></span>

## <span data-ttu-id="1eb17-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1eb17-144">RELATED LINKS</span></span>
