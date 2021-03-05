---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: cd904a913ce9ea0cdcc2d347463fa21ac7e13943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005206"
---
# <span data-ttu-id="861fe-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="861fe-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="861fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="861fe-102">SYNOPSIS</span></span>
<span data-ttu-id="861fe-103">Új felhasználót hoz létre az eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="861fe-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="861fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="861fe-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="861fe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="861fe-105">DESCRIPTION</span></span>
<span data-ttu-id="861fe-106">A **New-AzStackEdgeUser** parancsmag létrehoz egy új felhasználót a Stack Edge eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="861fe-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="861fe-107">Csak a típusú felhasználók `Share` létrehozása támogatott.</span><span class="sxs-lookup"><span data-stu-id="861fe-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="861fe-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="861fe-108">EXAMPLES</span></span>

### <span data-ttu-id="861fe-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="861fe-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="861fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="861fe-110">PARAMETERS</span></span>

### <span data-ttu-id="861fe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="861fe-111">-AsJob</span></span>
<span data-ttu-id="861fe-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="861fe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="861fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861fe-113">-DefaultProfile</span></span>
<span data-ttu-id="861fe-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="861fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="861fe-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="861fe-115">-DeviceName</span></span>
<span data-ttu-id="861fe-116">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="861fe-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861fe-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="861fe-117">-EncryptionKey</span></span>
<span data-ttu-id="861fe-118">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="861fe-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="861fe-119">-Name</span><span class="sxs-lookup"><span data-stu-id="861fe-119">-Name</span></span>
<span data-ttu-id="861fe-120">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="861fe-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861fe-121">-Password</span><span class="sxs-lookup"><span data-stu-id="861fe-121">-Password</span></span>
<span data-ttu-id="861fe-122">Jelszó megadása biztonságos karakterláncként</span><span class="sxs-lookup"><span data-stu-id="861fe-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="861fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="861fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="861fe-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="861fe-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861fe-125">-Type</span><span class="sxs-lookup"><span data-stu-id="861fe-125">-Type</span></span>
<span data-ttu-id="861fe-126">Select UserType</span><span class="sxs-lookup"><span data-stu-id="861fe-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861fe-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="861fe-127">-Confirm</span></span>
<span data-ttu-id="861fe-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="861fe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="861fe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="861fe-129">-WhatIf</span></span>
<span data-ttu-id="861fe-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="861fe-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="861fe-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="861fe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="861fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861fe-132">CommonParameters</span></span>
<span data-ttu-id="861fe-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="861fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861fe-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="861fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861fe-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="861fe-135">INPUTS</span></span>

### <span data-ttu-id="861fe-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="861fe-136">None</span></span>

## <span data-ttu-id="861fe-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="861fe-137">OUTPUTS</span></span>

### <span data-ttu-id="861fe-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="861fe-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="861fe-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="861fe-139">NOTES</span></span>

## <span data-ttu-id="861fe-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="861fe-140">RELATED LINKS</span></span>
