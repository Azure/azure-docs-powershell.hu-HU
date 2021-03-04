---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: b5d5da8c02081437f064fc1d2a6a29a5b772e8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001430"
---
# <span data-ttu-id="d4d23-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d4d23-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="d4d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4d23-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d23-103">Egy adott felügyelt HSM szerepkördefinícióit adott hatókörben sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d4d23-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="d4d23-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4d23-104">SYNTAX</span></span>

### <span data-ttu-id="d4d23-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4d23-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4d23-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d4d23-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4d23-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4d23-107">DESCRIPTION</span></span>
<span data-ttu-id="d4d23-108">Egy adott felügyelt HSM szerepkördefinícióit adott hatókörben sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d4d23-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="d4d23-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4d23-109">EXAMPLES</span></span>

### <span data-ttu-id="d4d23-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d4d23-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="d4d23-111">A példa az összes szerepkört a "/keys" hatókörben sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d4d23-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="d4d23-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4d23-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzKeyVaultRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="d4d23-113">A példa beszerzi a "Felügyelt biztonsági mentés" szerepkört, és ráveszi az engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="d4d23-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="d4d23-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4d23-114">PARAMETERS</span></span>

### <span data-ttu-id="d4d23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d23-115">-DefaultProfile</span></span>
<span data-ttu-id="d4d23-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4d23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4d23-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="d4d23-117">-HsmName</span></span>
<span data-ttu-id="d4d23-118">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="d4d23-118">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d23-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d4d23-119">-RoleDefinitionName</span></span>
<span data-ttu-id="d4d23-120">A lekért szerepkördefiníció neve.</span><span class="sxs-lookup"><span data-stu-id="d4d23-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d23-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="d4d23-121">-Scope</span></span>
<span data-ttu-id="d4d23-122">A szerepkör-hozzárendelés vagy -definíció hatóköre, például "/" vagy "/keys" vagy "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="d4d23-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="d4d23-123">A "/" akkor használatos, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="d4d23-123">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d23-124">CommonParameters</span></span>
<span data-ttu-id="d4d23-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d23-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4d23-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d23-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4d23-127">INPUTS</span></span>

### <span data-ttu-id="d4d23-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d4d23-128">None</span></span>

## <span data-ttu-id="d4d23-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4d23-129">OUTPUTS</span></span>

### <span data-ttu-id="d4d23-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d4d23-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="d4d23-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4d23-131">NOTES</span></span>

## <span data-ttu-id="d4d23-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4d23-132">RELATED LINKS</span></span>
