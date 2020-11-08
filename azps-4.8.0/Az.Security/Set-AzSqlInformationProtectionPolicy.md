---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180870"
---
# <span data-ttu-id="2d093-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d093-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="2d093-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d093-102">SYNOPSIS</span></span>
<span data-ttu-id="2d093-103">Az effektív bérlői SQL-adatvédelemi házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="2d093-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="2d093-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d093-104">SYNTAX</span></span>

### <span data-ttu-id="2d093-105">SQL-adatvédelemi házirend (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d093-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d093-106">SQL-adatvédelemi házirend fájlelérési útja</span><span class="sxs-lookup"><span data-stu-id="2d093-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d093-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d093-107">DESCRIPTION</span></span>
<span data-ttu-id="2d093-108">Az effektív bérlői SQL-adatvédelemi házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="2d093-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="2d093-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2d093-109">EXAMPLES</span></span>

### <span data-ttu-id="2d093-110">Például</span><span class="sxs-lookup"><span data-stu-id="2d093-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="2d093-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d093-111">PARAMETERS</span></span>

### <span data-ttu-id="2d093-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d093-112">-AsJob</span></span>
<span data-ttu-id="2d093-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2d093-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d093-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d093-114">-DefaultProfile</span></span>
<span data-ttu-id="2d093-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d093-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d093-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="2d093-116">-FilePath</span></span>
<span data-ttu-id="2d093-117">Az SQL-adatvédelem házirendjének definícióját tartalmazó. JSON fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d093-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="2d093-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="2d093-118">-Policy</span></span>
<span data-ttu-id="2d093-119">SQL-adatvédelemre vonatkozó házirend-definíciót ad meg.</span><span class="sxs-lookup"><span data-stu-id="2d093-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="2d093-120">Megadhatja a. JSON fájlok elérési útját, vagy egy JSON formátumú karakterláncot, amely meghatározza a házirendet.</span><span class="sxs-lookup"><span data-stu-id="2d093-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="2d093-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d093-121">-Confirm</span></span>
<span data-ttu-id="2d093-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d093-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d093-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d093-123">-WhatIf</span></span>
<span data-ttu-id="2d093-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d093-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d093-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d093-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d093-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d093-126">CommonParameters</span></span>
<span data-ttu-id="2d093-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d093-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d093-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2d093-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d093-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d093-129">INPUTS</span></span>

### <span data-ttu-id="2d093-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d093-130">System.String</span></span>

## <span data-ttu-id="2d093-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d093-131">OUTPUTS</span></span>

### <span data-ttu-id="2d093-132">Microsoft. Azure. Command. SecurityCenter. models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d093-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="2d093-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d093-133">NOTES</span></span>

## <span data-ttu-id="2d093-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d093-134">RELATED LINKS</span></span>
