---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345978"
---
# <span data-ttu-id="8e77d-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8e77d-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="8e77d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e77d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e77d-103">Új jelszót állít be egy felhasználónak az eszközön.</span><span class="sxs-lookup"><span data-stu-id="8e77d-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="8e77d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e77d-104">SYNTAX</span></span>

### <span data-ttu-id="8e77d-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e77d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e77d-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e77d-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e77d-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e77d-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e77d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e77d-108">DESCRIPTION</span></span>
<span data-ttu-id="8e77d-109">A **Set-AzDataBoxEdgeUser** parancsmag új jelszót állít be egy felhasználónak az Adatmező Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="8e77d-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="8e77d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e77d-110">EXAMPLES</span></span>

### <span data-ttu-id="8e77d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e77d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="8e77d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e77d-112">PARAMETERS</span></span>

### <span data-ttu-id="8e77d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e77d-113">-AsJob</span></span>
<span data-ttu-id="8e77d-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8e77d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e77d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e77d-115">-DefaultProfile</span></span>
<span data-ttu-id="8e77d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e77d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e77d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8e77d-117">-DeviceName</span></span>
<span data-ttu-id="8e77d-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="8e77d-118">Device Name</span></span>

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

### <span data-ttu-id="8e77d-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8e77d-119">-EncryptionKey</span></span>
<span data-ttu-id="8e77d-120">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="8e77d-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="8e77d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e77d-121">-InputObject</span></span>
<span data-ttu-id="8e77d-122">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="8e77d-122">Input Object</span></span>

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

### <span data-ttu-id="8e77d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8e77d-123">-Name</span></span>
<span data-ttu-id="8e77d-124">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="8e77d-124">Username</span></span>

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

### <span data-ttu-id="8e77d-125">-Password</span><span class="sxs-lookup"><span data-stu-id="8e77d-125">-Password</span></span>
<span data-ttu-id="8e77d-126">Jelszó megadása biztonságos karakterláncként</span><span class="sxs-lookup"><span data-stu-id="8e77d-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="8e77d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e77d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e77d-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8e77d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="8e77d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e77d-129">-ResourceId</span></span>
<span data-ttu-id="8e77d-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e77d-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="8e77d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e77d-131">-Confirm</span></span>
<span data-ttu-id="8e77d-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e77d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e77d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e77d-133">-WhatIf</span></span>
<span data-ttu-id="8e77d-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e77d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e77d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e77d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e77d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e77d-136">CommonParameters</span></span>
<span data-ttu-id="8e77d-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e77d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e77d-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e77d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e77d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e77d-139">INPUTS</span></span>

### <span data-ttu-id="8e77d-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e77d-140">None</span></span>

## <span data-ttu-id="8e77d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e77d-141">OUTPUTS</span></span>

### <span data-ttu-id="8e77d-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8e77d-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="8e77d-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e77d-143">NOTES</span></span>

## <span data-ttu-id="8e77d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e77d-144">RELATED LINKS</span></span>
