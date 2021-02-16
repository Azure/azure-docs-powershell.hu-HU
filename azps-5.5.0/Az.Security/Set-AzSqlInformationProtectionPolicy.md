---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169018"
---
# <span data-ttu-id="a1b37-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b37-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="a1b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b37-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b37-103">Beállítja a bérlői SQL-adatvédelemre vonatkozó hatékony házirendet.</span><span class="sxs-lookup"><span data-stu-id="a1b37-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="a1b37-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1b37-104">SYNTAX</span></span>

### <span data-ttu-id="a1b37-105">SQL Information Protection Policy (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1b37-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b37-106">SQL Information Protection Policy File Path</span><span class="sxs-lookup"><span data-stu-id="a1b37-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b37-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1b37-107">DESCRIPTION</span></span>
<span data-ttu-id="a1b37-108">Beállítja a bérlői SQL-adatvédelemre vonatkozó hatékony házirendet.</span><span class="sxs-lookup"><span data-stu-id="a1b37-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="a1b37-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1b37-109">EXAMPLES</span></span>

### <span data-ttu-id="a1b37-110">Példa</span><span class="sxs-lookup"><span data-stu-id="a1b37-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="a1b37-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1b37-111">PARAMETERS</span></span>

### <span data-ttu-id="a1b37-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1b37-112">-AsJob</span></span>
<span data-ttu-id="a1b37-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a1b37-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1b37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b37-114">-DefaultProfile</span></span>
<span data-ttu-id="a1b37-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1b37-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b37-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="a1b37-116">-FilePath</span></span>
<span data-ttu-id="a1b37-117">Az SQL Information Protection Policy definícióját tartalmazó .json fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1b37-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b37-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="a1b37-118">-Policy</span></span>
<span data-ttu-id="a1b37-119">Sql-adatvédelmi házirend-definíciót ad meg.</span><span class="sxs-lookup"><span data-stu-id="a1b37-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="a1b37-120">Megadhatja a házirendet definiáló .json fájl vagy JSON formátumú karakterlánc elérési útját.</span><span class="sxs-lookup"><span data-stu-id="a1b37-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b37-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1b37-121">-Confirm</span></span>
<span data-ttu-id="a1b37-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1b37-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b37-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b37-123">-WhatIf</span></span>
<span data-ttu-id="a1b37-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1b37-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1b37-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1b37-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b37-126">CommonParameters</span></span>
<span data-ttu-id="a1b37-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b37-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1b37-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b37-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1b37-129">INPUTS</span></span>

### <span data-ttu-id="a1b37-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a1b37-130">System.String</span></span>

## <span data-ttu-id="a1b37-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1b37-131">OUTPUTS</span></span>

### <span data-ttu-id="a1b37-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b37-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="a1b37-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1b37-133">NOTES</span></span>

## <span data-ttu-id="a1b37-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1b37-134">RELATED LINKS</span></span>
