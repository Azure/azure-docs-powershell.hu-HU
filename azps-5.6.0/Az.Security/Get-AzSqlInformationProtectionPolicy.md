---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: da881ceac74810b05385b26f54b7c498c60c2e77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936609"
---
# <span data-ttu-id="1a547-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a547-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="1a547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a547-102">SYNOPSIS</span></span>
<span data-ttu-id="1a547-103">Beolvassa a bérlőre vonatkozó hatékony SQL-adatvédelmi házirendet.</span><span class="sxs-lookup"><span data-stu-id="1a547-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="1a547-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1a547-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a547-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1a547-105">DESCRIPTION</span></span>
<span data-ttu-id="1a547-106">Beolvassa a bérlőre vonatkozó hatékony SQL-adatvédelmi házirendet.</span><span class="sxs-lookup"><span data-stu-id="1a547-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="1a547-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1a547-107">EXAMPLES</span></span>

### <span data-ttu-id="1a547-108">Példa</span><span class="sxs-lookup"><span data-stu-id="1a547-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="1a547-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a547-109">PARAMETERS</span></span>

### <span data-ttu-id="1a547-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a547-110">-AsJob</span></span>
<span data-ttu-id="1a547-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1a547-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a547-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a547-112">-DefaultProfile</span></span>
<span data-ttu-id="1a547-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a547-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a547-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a547-114">CommonParameters</span></span>
<span data-ttu-id="1a547-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a547-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a547-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a547-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a547-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a547-117">INPUTS</span></span>

### <span data-ttu-id="1a547-118">System.string</span><span class="sxs-lookup"><span data-stu-id="1a547-118">System.string</span></span>

## <span data-ttu-id="1a547-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a547-119">OUTPUTS</span></span>

### <span data-ttu-id="1a547-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a547-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="1a547-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1a547-121">NOTES</span></span>

## <span data-ttu-id="1a547-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a547-122">RELATED LINKS</span></span>
