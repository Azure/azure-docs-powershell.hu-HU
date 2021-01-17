---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337409"
---
# <span data-ttu-id="19bac-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="19bac-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="19bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19bac-102">SYNOPSIS</span></span>
<span data-ttu-id="19bac-103">Beolvassa a bérlőre vonatkozó hatékony SQL-adatvédelmi házirendet.</span><span class="sxs-lookup"><span data-stu-id="19bac-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="19bac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19bac-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19bac-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19bac-105">DESCRIPTION</span></span>
<span data-ttu-id="19bac-106">Beolvassa a bérlőre vonatkozó hatékony SQL-adatvédelmi házirendet.</span><span class="sxs-lookup"><span data-stu-id="19bac-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="19bac-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19bac-107">EXAMPLES</span></span>

### <span data-ttu-id="19bac-108">Példa</span><span class="sxs-lookup"><span data-stu-id="19bac-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="19bac-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19bac-109">PARAMETERS</span></span>

### <span data-ttu-id="19bac-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19bac-110">-AsJob</span></span>
<span data-ttu-id="19bac-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="19bac-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19bac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19bac-112">-DefaultProfile</span></span>
<span data-ttu-id="19bac-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19bac-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19bac-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bac-114">CommonParameters</span></span>
<span data-ttu-id="19bac-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19bac-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bac-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19bac-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bac-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19bac-117">INPUTS</span></span>

### <span data-ttu-id="19bac-118">System.string</span><span class="sxs-lookup"><span data-stu-id="19bac-118">System.string</span></span>

## <span data-ttu-id="19bac-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19bac-119">OUTPUTS</span></span>

### <span data-ttu-id="19bac-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="19bac-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="19bac-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19bac-121">NOTES</span></span>

## <span data-ttu-id="19bac-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19bac-122">RELATED LINKS</span></span>
