---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298736"
---
# <span data-ttu-id="3b4dd-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3b4dd-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="3b4dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4dd-103">Új felhasználó létrehozása az eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="3b4dd-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="3b4dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b4dd-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b4dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="3b4dd-106">A **New-AzDataBoxEdgeUser** parancsmag létrehoz egy új felhasználót az adatmező szélén lévő eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="3b4dd-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="3b4dd-107">Csak a típusú felhasználók létrehozása `Share` támogatott.</span><span class="sxs-lookup"><span data-stu-id="3b4dd-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="3b4dd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3b4dd-108">EXAMPLES</span></span>

### <span data-ttu-id="3b4dd-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b4dd-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="3b4dd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b4dd-110">PARAMETERS</span></span>

### <span data-ttu-id="3b4dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b4dd-111">-AsJob</span></span>
<span data-ttu-id="3b4dd-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3b4dd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b4dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4dd-113">-DefaultProfile</span></span>
<span data-ttu-id="3b4dd-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b4dd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b4dd-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3b4dd-115">-DeviceName</span></span>
<span data-ttu-id="3b4dd-116">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="3b4dd-116">Device Name</span></span>

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

### <span data-ttu-id="3b4dd-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3b4dd-117">-EncryptionKey</span></span>
<span data-ttu-id="3b4dd-118">Az Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="3b4dd-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="3b4dd-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b4dd-119">-Name</span></span>
<span data-ttu-id="3b4dd-120">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="3b4dd-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4dd-121">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="3b4dd-121">-Password</span></span>
<span data-ttu-id="3b4dd-122">Jelszó – biztonságos karakterlánc biztosítása</span><span class="sxs-lookup"><span data-stu-id="3b4dd-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="3b4dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b4dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b4dd-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3b4dd-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4dd-125">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="3b4dd-125">-Type</span></span>
<span data-ttu-id="3b4dd-126">UserType kijelölése</span><span class="sxs-lookup"><span data-stu-id="3b4dd-126">Select UserType</span></span>

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

### <span data-ttu-id="3b4dd-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b4dd-127">-Confirm</span></span>
<span data-ttu-id="3b4dd-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b4dd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b4dd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b4dd-129">-WhatIf</span></span>
<span data-ttu-id="3b4dd-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b4dd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b4dd-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b4dd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b4dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4dd-132">CommonParameters</span></span>
<span data-ttu-id="3b4dd-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b4dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4dd-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3b4dd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4dd-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b4dd-135">INPUTS</span></span>

### <span data-ttu-id="3b4dd-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="3b4dd-136">None</span></span>

## <span data-ttu-id="3b4dd-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b4dd-137">OUTPUTS</span></span>

### <span data-ttu-id="3b4dd-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3b4dd-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="3b4dd-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b4dd-139">NOTES</span></span>

## <span data-ttu-id="3b4dd-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b4dd-140">RELATED LINKS</span></span>
