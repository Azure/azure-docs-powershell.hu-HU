---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017632"
---
# <span data-ttu-id="3b823-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3b823-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="3b823-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b823-102">SYNOPSIS</span></span>
<span data-ttu-id="3b823-103">Visszanyeri a tényleges bérlői SQL-adatvédelemi házirendet.</span><span class="sxs-lookup"><span data-stu-id="3b823-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="3b823-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b823-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b823-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b823-105">DESCRIPTION</span></span>
<span data-ttu-id="3b823-106">Visszanyeri a tényleges bérlői SQL-adatvédelemi házirendet.</span><span class="sxs-lookup"><span data-stu-id="3b823-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="3b823-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b823-107">EXAMPLES</span></span>

### <span data-ttu-id="3b823-108">Például</span><span class="sxs-lookup"><span data-stu-id="3b823-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="3b823-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b823-109">PARAMETERS</span></span>

### <span data-ttu-id="3b823-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b823-110">-AsJob</span></span>
<span data-ttu-id="3b823-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3b823-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b823-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b823-112">-DefaultProfile</span></span>
<span data-ttu-id="3b823-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b823-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b823-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b823-114">CommonParameters</span></span>
<span data-ttu-id="3b823-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b823-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b823-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3b823-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b823-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b823-117">INPUTS</span></span>

### <span data-ttu-id="3b823-118">System. String</span><span class="sxs-lookup"><span data-stu-id="3b823-118">System.string</span></span>

## <span data-ttu-id="3b823-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b823-119">OUTPUTS</span></span>

### <span data-ttu-id="3b823-120">Microsoft. Azure. Command. SecurityCenter. models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3b823-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="3b823-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b823-121">NOTES</span></span>

## <span data-ttu-id="3b823-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b823-122">RELATED LINKS</span></span>
